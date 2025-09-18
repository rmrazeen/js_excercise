# Exercise 9: ES6 Features (Arrow Functions, Template Literals, Destructuring)

**Goal**: Practice modern JavaScript features introduced in ES6.

```js
// Arrow Functions (revisited)
const greet = name => `Hello, ${name}!`;
console.log(greet("Charlie"));

// Template Literals
const item = "Laptop";
const price = 1200;
const message = `The ${item} costs $${price}.`;
console.log(message);

// Array Destructuring
const numbers = [10, 20, 30];
const [first, second, third] = numbers;
console.log(`First: ${first}, Second: ${second}, Third: ${third}`);

// Object Destructuring
const user = {
  id: 1,
  username: "js_dev",
  email: "js@example.com"
};
const { username, email } = user;
console.log(`Username: ${username}, Email: ${email}`);

// Spread Operator for arrays
const arr1 = [1, 2];
const arr2 = [3, 4];
const combinedArr = [...arr1, ...arr2];
console.log("Combined Array:", combinedArr); // [1, 2, 3, 4]

// Spread Operator for objects
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };
const combinedObj = { ...obj1, ...obj2 };
console.log("Combined Object:", combinedObj); // { a: 1, b: 2, c: 3, d: 4 }
```

**What to learn**: Arrow functions, template literals, array destructuring, object destructuring, spread operator.
