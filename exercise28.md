# JavaScript Exercise 8 (Hard)

## Problem: Implement a custom `Array.prototype.filter`

Create a function `customFilter` that mimics the behavior of `Array.prototype.filter`. It should take an array and a callback function as arguments, and return a new array containing only the elements for which the callback function returns `true`.

### Example Usage:

```javascript
const numbers = [1, 2, 3, 4, 5, 6];
const evenNumbers = customFilter(numbers, (num) => num % 2 === 0);
console.log(evenNumbers); // Expected: [2, 4, 6]

const words = ["apple", "banana", "grape", "kiwi"];
const longWords = customFilter(words, (word) => word.length > 5);
console.log(longWords); // Expected: ["banana"]
```

### Solution Structure:

```javascript
function customFilter(arr, callback) {
  const result = [];
  for (let i = 0; i < arr.length; i++) {
    if (callback(arr[i], i, arr)) {
      result.push(arr[i]);
    }
  }
  return result;
}
