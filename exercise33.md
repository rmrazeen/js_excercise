# Exercise 4: Conditional Statements

**Goal**: Use `if`, `else if`, and `else` statements to control program flow based on conditions.

```js
let temperature = 25;

if (temperature < 0) {
  console.log("It's freezing!");
} else if (temperature >= 0 && temperature < 15) {
  console.log("It's cold.");
} else if (temperature >= 15 && temperature < 25) {
  console.log("It's mild.");
} else {
  console.log("It's hot!");
}

let day = "Sunday";

switch (day) {
  case "Monday":
    console.log("Start of the week.");
    break;
  case "Friday":
    console.log("Almost weekend!");
    break;
  case "Sunday":
    console.log("Relaxing day.");
    break;
  default:
    console.log("Mid-week day.");
}
```

**What to learn**: Conditional logic, `if/else if/else` structure, `switch` statement for multiple conditions.
