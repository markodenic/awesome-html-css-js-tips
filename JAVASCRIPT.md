# Awesome JavaScript Tips ![Awesome][awesome-badge]

#### Contents

- [Shorten an array](#shorten-an-array)
- [Short-circuits conditionals](#short-circuits-conditionals)
- [Assigning the remaining part of an array](#assigning-the-remaining-part-of-an-array)
- [Object property assigning to a variable with a different name](#object-property-assigning-to-a-variable-with-a-different-name)
- [Select a subset of columns to display when doing console.table()](#select-a-subset-of-columns-to-display-when-doing-consoletable)
- [Remove duplicate elements from the array](#remove-duplicate-elements-from-the-array)
- [Remove all falsy values from an array](#remove-all-falsy-values-from-an-array)
- [Convert a number to string](#convert-a-number-to-string)
- [Convert a numeric string to number](#convert-a-numeric-string-to-number)
- [Calculate the sum of all elements in array](#calculate-the-sum-of-all-elements-in-array)
- [Use template literals to concatenate strings](#use-template-literals-to-concatenate-strings)
- [Get the maximum of an array](#get-the-maximum-of-an-array)
- [Transform the array elements using the map function](#transform-the-array-elements-using-the-map-function)
- [Calculate the running sum of an array with currying](#calculate-the-running-sum-of-an-array-with-currying)

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

## Remove all falsy values from an array

```javascript
const myArray = [1, undefined, NaN, 2, null, '@denicmarko', true, 3, false];
console.log(myArray.filter(Boolean)); // [1, 2, '@denicmarko', true, 3]
```

## Convert a number to string

```javascript
const number = 403;
console.log(number + ''); // '403'
```

## Convert a numeric string to number

```javascript
const numericString = '403';
console.log(+ numericString); // 403
```

## Calculate the sum of all elements in array

You can use `reduce` method to calculate the sum of all elements in array:

```javascript
const myArray = [10, 20, 30, 40];
const reducer = (total, currentValue) => total + currentValue;
console.log(myArray.reduce(reducer)); // 100
```

## Use template literals to concatenate strings

```javascript
let name = 'Horse';
console.log(`The ${name} is sleeping`); // the Horse is sleeping 
```

## Get the maximum of an array

```javascript
let arr = [3, 5, 1];
console.log(Math.max(...arr)); // 5
```

## Transform the array elements using the map function

 ```javascript
const myArray = [1,2,3,4];

console.log(myArray.map(value => value * 2)); // [2, 4, 6, 8]
```

## Calculate the running sum of an array with currying

Here, a function is called with the initial `sum` value of zero that returns a function which accumulates the values of `myArray`.

```javascript
const myArray = [1,1,1,1];

console.log(myArray.map((sum => value => sum += value)(0))); // [1, 2, 3, 4]
```

[awesome-badge]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
