---
title: "I wish I know this before learn flutter"
date: 2023-07-04T08:18:24+07:00
draft: false
cover:
  image: ""
  alt: ""
  relative: false # To use relative path for cover image, used in hugo Page-bundles
---

# Cheatsheet Flutter

I was learn flutter on 2020 and then 2023 re-learn. Below is cheatsheet help you faster to learn flutter.

## **UI**

- Don't use regular component, use [`Sliver`](https://docs.flutter.dev/ui/advanced/slivers) instead
- Don't use regular Routing, use `go-router` instead

## **State Management**

- Use [Bloc](https://bloclibrary.dev/) for optimal solution.

## **Local Database**

- SQL
- No sql

## **Database Lib**

- Sqflite (Low Level)
- [Sqlite3](https://pub.dev/packages/sqlite3)
- [drift](https://pub.dev/packages/drift) (SQL - ORM)
- [Floor](https://pub.dev/packages/floor) (SQL - ORM)
- [Hive](https://pub.dev/packages/hive) (No sql)
- [ObjectBox](https://pub.dev/packages/objectbox) (No Sql)

## **Environtment**

- [Flutter DotEnv](https://pub.dev/packages/flutter_dotenv)
- [Envied](https://pub.dev/packages/envied) (Class)
WIP Flutter env built-in support : [Add .env file support for option `--dart-define-from-file`](https://github.com/flutter/flutter/pull/128668).

## Test

- [Mockito](https://pub.dev/packages/mockito) (code generator)
- [Mocktail](https://pub.dev/packages/mocktail) (simple API)
- [Bloc Test](https://pub.dev/packages/bloc_test)

### Dart define

[Article discuss about `--dart-deffine-from-file`](https://gboliknow.medium.com/efficiently-configuring-your-flutter-app-with-dart-define-from-file-604d9bd49e7b). but there is no original documentation for this cli
Other [blog](https://itnext.io/flutter-3-7-and-a-new-way-of-defining-compile-time-variables-f63db8a4f6e2), but the env too complicated, need configuration at native layer too (android gradle, and ios)

## Icon

Use [flutter_launcher_icons package](https://pub.dev/packages/flutter_launcher_icons).

## More info

Read [Deployment info](https://docs.flutter.dev/deployment) for each platform.