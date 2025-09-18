# JavaScript Exercise 4 (Hard)

## Problem: Implement a deep clone function

Create a function `deepClone` that performs a deep copy of a given value. The function should handle primitive types, arrays, objects, and circular references.

### Example Usage:

```javascript
const obj1 = {
  a: 1,
  b: {
    c: 2
  },
  d: [3, 4]
};
obj1.e = obj1; // Circular reference

const obj2 = deepClone(obj1);

console.log(obj2);
console.log(obj1 === obj2); // Expected: false
console.log(obj1.b === obj2.b); // Expected: false
console.log(obj1.d === obj2.d); // Expected: false
console.log(obj2.e === obj2); // Expected: true (circular reference maintained)
```

### Solution Structure:

```javascript
function deepClone(value, hash = new WeakMap()) {
  if (Object(value) !== value) return value; // Primitive values
  if (hash.has(value)) return hash.get(value); // Circular reference

  const result = Array.isArray(value) ? [] : {};
  hash.set(value, result);

  for (const key in value) {
    if (Object.prototype.hasOwnProperty.call(value, key)) {
      result[key] = deepClone(value[key], hash);
    }
  }

  return result;
}
