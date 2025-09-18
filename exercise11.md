# Medium Exercise 1: Count Vowels

**Goal**: Write a JavaScript function that takes a string and returns the count of vowels (a, e, i, o, u) in it. Case-insensitive.

```js
function countVowels(str) {
  const vowels = "aeiou";
  let count = 0;
  for (let char of str.toLowerCase()) {
    if (vowels.includes(char)) {
      count++;
    }
  }
  return count;
}

console.log("Vowels in 'hello':", countVowels("hello")); // Expected: 2
console.log("Vowels in 'JavaScript':", countVowels("JavaScript")); // Expected: 3
console.log("Vowels in 'rhythm':", countVowels("rhythm")); // Expected: 0
```

**What to learn**: String iteration, `toLowerCase()`, `includes()`, counter variable.
