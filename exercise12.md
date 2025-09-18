# Medium Exercise 2: Remove Duplicates from Array

**Goal**: Write a JavaScript function that takes an array and returns a new array with duplicate elements removed.

```js
function removeDuplicates(arr) {
  return [...new Set(arr)];
}

console.log("Original: [1, 2, 2, 3, 4, 4, 5], Unique:", removeDuplicates([1, 2, 2, 3, 4, 4, 5])); // Expected: [1, 2, 3, 4, 5]
console.log("Original: ['a', 'b', 'a', 'c'], Unique:", removeDuplicates(['a', 'b', 'a', 'c'])); // Expected: ['a', 'b', 'c']
console.log("Original: [], Unique:", removeDuplicates([])); // Expected: []
```

**What to learn**: `Set` object for uniqueness, spread operator (`...`).
