# Medium Exercise 8: Find Missing Number

**Goal**: Write a JavaScript function that takes an array containing `n` distinct numbers taken from `0, 1, 2, ..., n` and returns the one that is missing from the array.

```js
function findMissingNumber(nums) {
  const n = nums.length;
  const expectedSum = n * (n + 1) / 2;
  const actualSum = nums.reduce((sum, num) => sum + num, 0);
  return expectedSum - actualSum;
}

console.log("Missing number in [3, 0, 1]:", findMissingNumber([3, 0, 1])); // Expected: 2
console.log("Missing number in [9, 6, 4, 2, 3, 5, 7, 0, 1]:", findMissingNumber([9, 6, 4, 2, 3, 5, 7, 0, 1])); // Expected: 8
console.log("Missing number in [0, 1]:", findMissingNumber([0, 1])); // Expected: 2
```

**What to learn**: Array `reduce()`, mathematical formulas for sum of series, array length.
