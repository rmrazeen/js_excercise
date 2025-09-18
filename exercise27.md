# JavaScript Exercise 7 (Hard)

## Problem: Implement a custom `Array.prototype.map`

Create a function `customMap` that mimics the behavior of `Array.prototype.map`. It should take an array and a callback function as arguments, and return a new array containing the results of calling the callback function on every element in the input array.

### Example Usage:

```javascript
const numbers = [1, 2, 3, 4];
const doubled = customMap(numbers, (num) => num * 2);
console.log(doubled); // Expected: [2, 4, 6, 8]

const strings = ["hello", "world"];
const uppercased = customMap(strings, (str) => str.toUpperCase());
console.log(uppercased); // Expected: ["HELLO", "WORLD"]
```

### Solution Structure:

```javascript
function customMap(arr, callback) {
  const result = [];
  for (let i = 0; i < arr.length; i++) {
    result.push(callback(arr[i], i, arr));
  }
  return result;
}
