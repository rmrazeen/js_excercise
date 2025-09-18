# Exercise 7: Arrays

**Goal**: Create and manipulate arrays using common array methods.

```js
let colors = ["red", "green", "blue"];

// Accessing elements
console.log("First color:", colors[0]); // red
console.log("Last color:", colors[colors.length - 1]); // blue

// Adding elements
colors.push("yellow"); // Add to the end
colors.unshift("purple"); // Add to the beginning
console.log("After adding:", colors); // ["purple", "red", "green", "blue", "yellow"]

// Removing elements
colors.pop(); // Remove from the end
colors.shift(); // Remove from the beginning
console.log("After removing:", colors); // ["red", "green", "blue"]

// Iterating with forEach
console.log("\nColors using forEach:");
colors.forEach(function(color) {
  console.log(color);
});

// Map method
let uppercaseColors = colors.map(color => color.toUpperCase());
console.log("Uppercase colors:", uppercaseColors); // ["RED", "GREEN", "BLUE"]

// Filter method
let colorsWithE = colors.filter(color => color.includes('e'));
console.log("Colors with 'e':", colorsWithE); // ["green", "blue"]
```

**What to learn**: Array creation, accessing elements, `push`, `pop`, `unshift`, `shift`, `forEach`, `map`, `filter` methods.
