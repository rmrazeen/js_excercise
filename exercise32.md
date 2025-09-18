# Exercise 3: Operators

**Goal**: Demonstrate the use of arithmetic, assignment, comparison, and logical operators.

```js
let a = 10;
let b = 5;

// Arithmetic Operators
console.log("a + b =", a + b); // 15
console.log("a - b =", a - b); // 5
console.log("a * b =", a * b); // 50
console.log("a / b =", a / b); // 2
console.log("a % b =", a % b); // 0

// Assignment Operators
let x = 20;
x += 5; // x = x + 5
console.log("x after x += 5:", x); // 25

// Comparison Operators
console.log("a > b :", a > b);   // true
console.log("a === 10 :", a === 10); // true
console.log("b !== '5' :", b !== '5'); // true (strict inequality)

// Logical Operators
let isAdult = true;
let hasLicense = false;
console.log("isAdult && hasLicense :", isAdult && hasLicense); // false
console.log("isAdult || hasLicense :", isAdult || hasLicense); // true
console.log("!isAdult :", !isAdult); // false
```

**What to learn**: Different types of operators and their precedence, how to perform calculations, comparisons, and logical operations.
