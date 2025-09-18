# Easy Exercise 3: Find the Larger Number

**Goal**: Write a JavaScript function that takes two numbers and returns the larger of the two.

```js
function findLarger(num1, num2) {
  if (num1 > num2) {
    return num1;
  } else {
    return num2;
  }
}

console.log("Larger of 7 and 12:", findLarger(7, 12)); // Expected: 12
console.log("Larger of 20 and 5:", findLarger(20, 5)); // Expected: 20
console.log("Larger of 8 and 8:", findLarger(8, 8)); // Expected: 8
```

**What to learn**: Conditional statements, comparison operators.
