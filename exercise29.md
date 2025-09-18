# JavaScript Exercise 9 (Hard)

## Problem: Implement a custom `Array.prototype.reduce`

Create a function `customReduce` that mimics the behavior of `Array.prototype.reduce`. It should take an array, a callback function, and an optional initial value as arguments. It should apply the callback function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

### Example Usage:

```javascript
const numbers = [1, 2, 3, 4];
const sum = customReduce(numbers, (acc, num) => acc + num, 0);
console.log(sum); // Expected: 10

const flattened = customReduce(
  [
    [0, 1],
    [2, 3],
    [4, 5]
  ],
  (acc, val) => acc.concat(val), []
);
console.log(flattened); // Expected: [0, 1, 2, 3, 4, 5]

const max = customReduce(numbers, (acc, num) => (num > acc ? num : acc));
console.log(max); // Expected: 4 (without initial value)
```

### Solution Structure:

```javascript
function customReduce(arr, callback, initialValue) {
  let accumulator = initialValue;
  let startIndex = 0;

  if (initialValue === undefined) {
    if (arr.length === 0) {
      throw new TypeError('Reduce of empty array with no initial value');
    }
    accumulator = arr[0];
    startIndex = 1;
  }

  for (let i = startIndex; i < arr.length; i++) {
    accumulator = callback(accumulator, arr[i], i, arr);
  }

  return accumulator;
}
