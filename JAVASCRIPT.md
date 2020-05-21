# Awesome JavaScript Tips ![Awesome][awesome-badge]

#### Contents

- [Shorten an array](#shorten-an-array)
- [Short-circuits conditionals](#short-circuits-conditionals)
- [Assigning the remaining part of an array](#assigning-the-remaining-part-of-an-array)
- [Object property assigning to a variable with a different name](#object-property-assigning-to-a-variable-with-a-different-name)
- [Select a subset of columns to display when doing console.table()](#select-a-subset-of-columns-to-display-when-doing-consoletable)
- [Remove duplicate elements from the array](#remove-duplicate-elements-from-the-array)

## Shorten an array

You can set the length property to shorten an array.

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.length = 3;

console.log(numbers); // Array(3) [1, 2, 3]
```

## Short-circuits conditionals

If you have to execute a function only if condition is true, you can use short-circuit.

```javascript
// Instead of this
if (condition) {
    doSomething();
}

// You can use short-circuit
condition && doSomething();
```

## Assigning the remaining part of an array

When destructuring an array, you can unpack and assign the remaining part of it to a variable using the rest pattern:

```javascript
const [a, ...b] = [1, 2, 3, 4, 5];
console.log(a); // 1
console.log(b); // [2, 3, 4, 5]
```

## Object property assigning to a variable with a different name

A property can be unpacked from an object and assigned to a variable with a different name than the object property:

```javascript
const obj = {a: 42, b: true};
const {a: foo, b: bar} = obj;
console.log(foo); // 42
console.log(bar); // true
```

## Select a subset of columns to display when doing console.table()

By default, `console.table()` lists all elements in each row. You can use the optional "columns" parameter to select a subset of columns to display:

```javascript
// an array of objects, logging only firstName
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const john = new Person("John", "Smith");
const jane = new Person("Jane", "Doe");

console.table([john, jane], ["firstName"]);
```

## Remove duplicate elements from the array

```javascript
const myArray = [5, 4, 3, 'a', 5, 5, 'a'];
console.log([... new Set(myArray)]); // [5, 4, 3, "a"]
```

[awesome-badge]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg

