# Easy Exercise 8: Factorial Calculation

**Goal**: Write a JavaScript function to calculate the factorial of a non-negative integer.

```js
function factorial(n) {
  if (n === 0 || n === 1) {
    return 1;
  } else if (n < 0) {
    return "Factorial is not defined for negative numbers.";
  } else {
    let result = 1;
    for (let i = 2; i <= n; i++) {
      result *= i;
    }
    return result;
  }
}

console.log("Factorial of 0:", factorial(0)); // Expected: 1
console.log("Factorial of 5:", factorial(5)); // Expected: 120 (5*4*3*2*1)
console.log("Factorial of 3:", factorial(3)); // Expected: 6 (3*2*1)
console.log("Factorial of -4:", factorial(-4)); // Expected: "Factorial is not defined for negative numbers."
```

**What to learn**: Loops, conditional statements, mathematical operations, handling edge cases.
