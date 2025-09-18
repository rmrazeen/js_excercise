# Easy Exercise 10: Find Maximum in Array

**Goal**: Write a JavaScript function that takes an array of numbers and returns the largest number in the array.

```js
function findMax(numbers) {
  if (numbers.length === 0) {
    return undefined; // Or throw an error, depending on desired behavior for empty arrays
  }
  let max = numbers[0];
  for (let i = 1; i < numbers.length; i++) {
    if (numbers[i] > max) {
      max = numbers[i];
    }
  }
  return max;
}

console.log("Max of [1, 5, 2, 8, 3]:", findMax([1, 5, 2, 8, 3])); // Expected: 8
console.log("Max of [-10, -5, -2]:", findMax([-10, -5, -2])); // Expected: -2
console.log("Max of []:", findMax([])); // Expected: undefined
```

**What to learn**: Array iteration, comparison, handling empty arrays.
