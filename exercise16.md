# Medium Exercise 6: Array Flatten

**Goal**: Write a JavaScript function that takes an array of arrays (nested arrays) and flattens it into a single array.

```js
function flattenArray(arr) {
  let flattened = [];
  for (let element of arr) {
    if (Array.isArray(element)) {
      flattened = flattened.concat(flattenArray(element)); // Recursive call for nested arrays
    } else {
      flattened.push(element);
    }
  }
  return flattened;
}

console.log("Flatten [[1, 2], [3, 4]]:", flattenArray([[1, 2], [3, 4]])); // Expected: [1, 2, 3, 4]
console.log("Flatten [1, [2, [3, 4]], 5]:", flattenArray([1, [2, [3, 4]], 5])); // Expected: [1, 2, 3, 4, 5]
console.log("Flatten []:", flattenArray([])); // Expected: []

// Alternative using flat() method (ES2019+)
// function flattenArrayBuiltIn(arr) {
//   return arr.flat(Infinity); // flat(Infinity) flattens all nested arrays
// }
// console.log("Flatten with built-in [[1, 2], [3, 4]]:", flattenArrayBuiltIn([[1, 2], [3, 4]]));
```

**What to learn**: Recursion, `Array.isArray()`, `concat()`, `push()`. (Optional: `flat()` method).
