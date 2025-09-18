# Medium Exercise 10: Fibonacci Sequence

**Goal**: Write a JavaScript function that generates the first `n` numbers of the Fibonacci sequence.

```js
function fibonacciSequence(n) {
  if (n <= 0) {
    return [];
  } else if (n === 1) {
    return [0];
  } else {
    let sequence = [0, 1];
    for (let i = 2; i < n; i++) {
      sequence.push(sequence[i - 1] + sequence[i - 2]);
    }
    return sequence;
  }
}

console.log("Fibonacci sequence for n=0:", fibonacciSequence(0)); // Expected: []
console.log("Fibonacci sequence for n=1:", fibonacciSequence(1)); // Expected: [0]
console.log("Fibonacci sequence for n=5:", fibonacciSequence(5)); // Expected: [0, 1, 1, 2, 3]
console.log("Fibonacci sequence for n=10:", fibonacciSequence(10)); // Expected: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```

**What to learn**: Loops, array manipulation (`push`), conditional statements, understanding recursive patterns.
