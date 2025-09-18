# Exercise 8: Objects

**Goal**: Create and manipulate objects, including accessing properties and iterating over them.

```js
let car = {
  make: "Toyota",
  model: "Camry",
  year: 2020,
  start: function() {
    console.log("Engine started!");
  },
  features: ["GPS", "Bluetooth", "Sunroof"]
};

// Accessing properties
console.log("Car make:", car.make); // Toyota
console.log("Car year:", car["year"]); // 2020

// Modifying properties
car.year = 2021;
console.log("Updated car year:", car.year); // 2021

// Adding new properties
car.color = "blue";
console.log("Car color:", car.color); // blue

// Calling object methods
car.start(); // Engine started!

// Iterating over object properties
console.log("\nCar properties:");
for (let key in car) {
  if (typeof car[key] !== 'function') { // Exclude functions
    console.log(`${key}: ${car[key]}`);
  }
}
```

**What to learn**: Object literal syntax, dot notation, bracket notation, adding/modifying properties, object methods, iterating with `for...in` loop.
