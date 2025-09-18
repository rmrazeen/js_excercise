# Medium Exercise 4: Capitalize First Letter

**Goal**: Write a JavaScript function that takes a string and returns a new string with the first letter of each word capitalized.

```js
function capitalizeWords(str) {
  return str.split(' ').map(word => {
    if (word.length === 0) return "";
    return word.charAt(0).toUpperCase() + word.slice(1).toLowerCase();
  }).join(' ');
}

console.log("Capitalize 'hello world':", capitalizeWords("hello world")); // Expected: "Hello World"
console.log("Capitalize 'javaScript is fun':", capitalizeWords("javaScript is fun")); // Expected: "Javascript Is Fun"
console.log("Capitalize 'a short sentence':", capitalizeWords("a short sentence")); // Expected: "A Short Sentence"
```

**What to learn**: String `split()`, `map()` array method, `charAt()`, `toUpperCase()`, `slice()`, `toLowerCase()`, `join()`.
