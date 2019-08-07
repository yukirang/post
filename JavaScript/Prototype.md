
## Prototype and Object Constructor
In JavaScript, all objects inherit properties and methods from a prototype. One way of creating a object in JavaScript is through the constructor function:

```
function Animal(){
  this.eat = () => {
    console.log('Animal eat.');
  }
}

function Dog(){
  this.bark = (name) => {
    console.log(`${name} bark.`);
  }
}

Dog.prototype = new Animal();
let puppy = new Dog('Nicole');
```

When new an object, one object will be created first, then this will point to the new object and related code in constructor would be executed (normally with the assignments this.properties=SOME_VALUE ). At last this will be returned.

## Facts about Prototype
1. Every reference type (array, object, function, except null) has the feature of an object, which is free extension.

2. Every type of variable in 1 has a __proto__(implicit prototype) property, the value of the property is a normal object.

3. Every type of variable in 1 has a prototype (explicit prototype) property, the value of the property is a normal object.

4. For every type of variable in 1, __proto__ is equal to prototype of its constructor

## Prototype Chain
When trying to get some property of an object, if the object itself doesn’t have this property, JavaScript will search through its __proto__, which forms a __proto__ chain. Based on 4 it’s easy to understand there is also a prototype chain.

## instanceof
instanceof tests whether a function is the constructor of an object. It goes through the prototype chain of an object and try to see whether the prototype property of a constructor appears.

```
let f = new Foo('123');
console.log(f instance of Foo);
```

What actually happens here is it will go through the __proto__ line of f and prototype line of Foo, if too lines points to the same object in the end , it will return true, otherwise, return false.

For me, prototype is one of the hardest topic in JavaScript. I believe with continuous learning and coding I can understand it more!