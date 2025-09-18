# Medium Exercise 3: Find Longest Word

**Goal**: Write a JavaScript function that takes a string of words and returns the longest word in the string.

```js
function findLongestWord(sentence) {
  const words = sentence.split(' ');
  let longestWord = "";
  for (let word of words) {
    if (word.length > longestWord.length) {
      longestWord = word;
    }
  }
  return longestWord;
}

console.log("Longest word in 'The quick brown fox jumped':", findLongestWord("The quick brown fox jumped")); // Expected: "jumped"
console.log("Longest word in 'hello world':", findLongestWord("hello world")); // Expected: "hello" (or "world")
console.log("Longest word in 'a b c':", findLongestWord("a b c")); // Expected: "a" (or "b" or "c")
```

**What to learn**: String `split()`, array iteration, string length, comparison.
