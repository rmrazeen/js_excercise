# Easy Exercise 9: Check Palindrome

**Goal**: Write a JavaScript function that checks if a given string is a palindrome (reads the same forwards and backwards).

```js
function isPalindrome(str) {
  const cleanedStr = str.toLowerCase().replace(/[^a-z0-9]/g, ''); // Remove non-alphanumeric and convert to lowercase
  const reversedStr = cleanedStr.split('').reverse().join('');
  return cleanedStr === reversedStr;
}

console.log("'madam' is a palindrome:", isPalindrome("madam")); // Expected: true
console.log("'hello' is a palindrome:", isPalindrome("hello")); // Expected: false
console.log("'A man, a plan, a canal: Panama' is a palindrome:", isPalindrome("A man, a plan, a canal: Panama")); // Expected: true
```

**What to learn**: String manipulation, `toLowerCase`, `replace`, `split`, `reverse`, `join` methods, comparison.
