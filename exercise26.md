# JavaScript Exercise 6 (Hard)

## Problem: Implement a `curry` function

Create a `curry` function that takes a function `func` as an argument and returns a curried version of that function. The curried function should accept arguments one at a time or in multiple calls until all expected arguments are provided, at which point the original function `func` should be executed.

### Example Usage:

```javascript
function sum(a, b, c) {
  return a + b + c;
}

const curriedSum = curry(sum);

console.log(curriedSum(1)(2)(3)); // Expected: 6
console.log(curriedSum(1, 2)(3)); // Expected: 6
console.log(curriedSum(1)(2, 3)); // Expected: 6
console.log(curriedSum(1, 2, 3)); // Expected: 6
```

### Solution Structure:

```javascript
function curry(func) {
  return function curried(...args) {
    if (args.length >= func.length) {
      return func.apply(this, args);
    } else {
      return function(...args2) {
        return curried.apply(this, args.concat(args2));
      };
    }
  };
}
