# Easy Exercise 2: Check Even or Odd

**Goal**: Write a JavaScript function that takes a number and returns "Even" if the number is even, and "Odd" if the number is odd.

```js
function checkEvenOrOdd(number) {
  if (number % 2 === 0) {
    return "Even";
  } else {
    return "Odd";
  }
}

console.log("5 is:", checkEvenOrOdd(5)); // Expected: Odd
console.log("10 is:", checkEvenOrOdd(10)); // Expected: Even
console.log("0 is:", checkEvenOrOdd(0)); // Expected: Even
```

**What to learn**: Conditional statements (`if/else`), modulo operator (`%`).
