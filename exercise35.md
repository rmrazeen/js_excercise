# Exercise 6: Functions

**Goal**: Define and call functions, including functions with parameters and return values.

```js
// Function without parameters
function greet() {
  console.log("Hello there!");
}
greet(); // Call the function

// Function with parameters
function greetUser(name) {
  console.log(`Hello, ${name}!`);
}
greetUser("Bob"); // Call with an argument

// Function with return value
function add(a, b) {
  return a + b;
}
let sum = add(5, 3);
console.log("Sum:", sum); // 8

// Arrow function (ES6+)
const multiply = (a, b) => a * b;
console.log("Product:", multiply(4, 2)); // 8
```

**What to learn**: Function declaration, function invocation, parameters, return values, arrow functions.
