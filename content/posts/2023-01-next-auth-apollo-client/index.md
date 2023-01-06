---
title: "Kombinasi Next-auth dan Apollo Client"
date: 2023-01-06T08:33:56+07:00
draft: true
cover:
  image: ""
  alt: ""
  relative: false # To use relative path for cover image, used in hugo Page-bundles
---

## Next-auth

[Next auth](https://next-auth.js.org/) adalah authentikasi untuk nextjs. Sangat powerfull dengan fitur yang ditawarkan

## Apollo Client

[Apollo Client](https://www.apollographql.com/) adalah apollo client untuk mengatur adapter graphql


## Ambil Token dari next-auth

Untuk mengirim authentikasi ke apollo client, kita perlu mengambil token. Tapi next-auth tidak menyimpan token di client (seperti localstorage), tapi tersimpan didalam cookies session. Berdasarkan [pernyatan ini](https://github.com/nextauthjs/next-auth/discussions/1492#discussioncomment-2177300). 

> session content is not stored in cookies, either. NextAuth creates a cookie named next-auth.session-token which stores the JWT, not the session object. IMO, it is not a good idea to store identity (session) and permissions/roles/claims (access_token) at the same place. I created a separate serverless function for this use case, and it supports silent refresh (when access_token expires).

Dari sini dapat terlihat jelas bahwa next-auth tidak menyimpan `access_token` di client, melainkan di session. Baiklah, biarkan begitu arsitektur authentikasi dan authorization.

## Menyimpan token di session Next-auth

Tambahkan callback `session` di file `[...nextauth].ts`. Didalamnya tambahkan `session.token` yang diisi dengan value jwt.

```ts
callbacks: {
    session: async ({ session, token }) => {
      if (session?.user) {
        session.user.id = token.sub!;
      }
      session.token = jsonwebtoken.sign(token, process.env.NEXTAUTH_SECRET || '')
      return session;
    },
  },
```

setelah itu, akan mudah untuk mendapatkan token dari client, bisa menggunakan `useSession` atau `getSession`

```js
const session = useSession()
session.token //jwt token

const session = await getSession() //async
session.token //jwt token
```

## Mengatur akses token untuk apollo client

Berikut contoh file apollo client. [Sumber contoh kode](https://github.com/nextauthjs/next-auth/discussions/1492#discussioncomment-781656)

```ts
import { ApolloClient, from, createHttpLink, InMemoryCache } from "@apollo/client";
import { environment } from "config";
import { setContext } from "@apollo/client/link/context";
import { getSession } from "next-auth/client";

const httpLink = createHttpLink({
	uri: environment.grapqlServerURL,
	credentials: "include",
});

const authLink = setContext(async (_, { headers }: { headers: Headers }) => {
	const session = await getSession();
	const modifiedHeader = {
		headers: {
			...headers,
			authorization: session?.accessToken
				? `Bearer ${session.accessToken}`
				: "",
      },
  };
  return modifiedHeader;
});

const client = new ApolloClient({
  link: from([authLink, httpLink]),
  cache: new InMemoryCache(),
});

export default client;
```

Untuk mendapatkan token, perlu menggunakan client api dari next-auth yaitu `getSession()`. Ini akan mengambil token dari Rest API `/api/auth/session`.


## Kesimpulan

Untuk mengambil token dan mengatur untuk apollo client, perlu diatur menggunakan beberapa kombinasi kode dan pengaturan. Awalnya ini cukup sulit diimplementasi karena next-auth dan apollo memiliki arsitektur yang berbeda, tapi karena fleksibilitas dan API yang tersedia ini dapat dilakukan.