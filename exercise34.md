# Exercise 5: Loops

**Goal**: Use `for` and `while` loops to iterate over a sequence of numbers or array elements.

```js
// For loop
console.log("For loop from 1 to 5:");
for (let i = 1; i <= 5; i++) {
  console.log(i);
}

// While loop
console.log("\nWhile loop from 5 to 1:");
let j = 5;
while (j >= 1) {
  console.log(j);
  j--;
}

// Iterating over an array
console.log("\nIterating over an array:");
const fruits = ["apple", "banana", "cherry"];
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}

// For...of loop (ES6+)
console.log("\nFor...of loop over an array:");
for (const fruit of fruits) {
  console.log(fruit);
}
```

**What to learn**: `for` loop, `while` loop, iterating over arrays, `for...of` loop.
