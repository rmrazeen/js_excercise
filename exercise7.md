# Easy Exercise 7: Reverse a String

**Goal**: Write a JavaScript function that takes a string and returns its reverse.

```js
function reverseString(str) {
  return str.split('').reverse().join('');
}

console.log("Reverse of 'hello':", reverseString("hello")); // Expected: "olleh"
console.log("Reverse of 'JavaScript':", reverseString("JavaScript")); // Expected: "tpircSavaJ"
console.log("Reverse of '':", reverseString("")); // Expected: ""
```

**What to learn**: String methods (`split`, `reverse`, `join`), array manipulation.
