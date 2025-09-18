# Easy Exercise 6: Array Sum

**Goal**: Write a JavaScript function that takes an array of numbers and returns the sum of all elements.

```js
function sumArray(numbers) {
  let total = 0;
  for (let i = 0; i < numbers.length; i++) {
    total += numbers[i];
  }
  return total;
}

console.log("Sum of [1, 2, 3]:", sumArray([1, 2, 3])); // Expected: 6
console.log("Sum of [10, -5, 15]:", sumArray([10, -5, 15])); // Expected: 20
console.log("Sum of []:", sumArray([])); // Expected: 0
```

**What to learn**: Array iteration (`for` loop), accumulating a sum.
