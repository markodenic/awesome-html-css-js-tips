# Awesome JavaScript Tips ![Awesome][awesome-badge]

#### Contents

- [Shorten an array](#shorten-an-array)
- [Short-circuits conditionals](#short-circuits-conditionals)

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

[awesome-badge]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg

