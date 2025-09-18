# Medium Exercise 7: Anagram Checker

**Goal**: Write a JavaScript function that takes two strings and determines if they are anagrams of each other.

```js
function areAnagrams(str1, str2) {
  const cleanStr = (str) => str.toLowerCase().replace(/[^a-z0-9]/g, '').split('').sort().join('');

  const cleanedStr1 = cleanStr(str1);
  const cleanedStr2 = cleanStr(str2);

  return cleanedStr1 === cleanedStr2;
}

console.log("'listen' and 'silent' are anagrams:", areAnagrams("listen", "silent")); // Expected: true
console.log("'hello' and 'world' are anagrams:", areAnagrams("hello", "world")); // Expected: false
console.log("'Debit card' and 'Bad credit' are anagrams:", areAnagrams("Debit card", "Bad credit")); // Expected: true
```

**What to learn**: String manipulation (`toLowerCase`, `replace`, `split`, `sort`, `join`), function helper, comparison.
