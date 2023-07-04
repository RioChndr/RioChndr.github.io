---
title: "You Should Use Dependency Injection for TDD"
date: 2023-07-04T08:35:48+07:00
draft: flase
tags: ['blogging']
cover:
  image: ""
  alt: ""
  relative: false # To use relative path for cover image, used in hugo Page-bundles
---

Let see this code

```js
class Car {
  whell = new Whell();
  run(){
    this.whell.move();
  }
}
```

How to make test to ensure the Car run whell correctly ?, above code is not possible to unit test. so we need to modify this code and create constructor to inject whell object.

```js
class Car {
  constructor(whell){
    this.whell = whell
  }
  run(){
    this.whell.move();
  }
}
```

with this code we can inject `mock whell` to make sure this code run correctly.

```js
it('Should run whell correctly', function() {
  const mockWhell = new MockWhell(); // example mock whell
  const car = new Car(mockWhell);
  car.run();

  assert(() => mockWhell.move(), shouldCalled(1)); // example
});
```

From the code above, we can conclude that, in order to create `test-able` code, we need access to other package injections. But it becomes a problem if there are many related packages, the constructor will be full of package objects.
Therefore DI (Dependency injection) is a solution, object construction is controlled by the framework and developers can create the desired mock class in the unit test code.
