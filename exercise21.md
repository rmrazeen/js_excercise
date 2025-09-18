# JavaScript Exercise 1 (Hard)

## Problem: Implement a `debounce` function

Create a `debounce` function that takes a function `func` and a `delay` as arguments. The `debounce` function should return a new function that, when invoked, will execute `func` only if `delay` milliseconds have passed since the last time it was invoked.

### Example Usage:

```javascript
function logMessage(message) {
  console.log(message);
}

const debouncedLog = debounce(logMessage, 1000);

debouncedLog("Hello"); // Will not execute immediately
debouncedLog("World"); // Will not execute immediately
// After 1 second, "World" should be logged (if no more calls)
```

### Solution Structure:

```javascript
function debounce(func, delay) {
  let timeoutId;

  return function(...args) {
    const context = this;
    clearTimeout(timeoutId);
    timeoutId = setTimeout(() => {
      func.apply(context, args);
    }, delay);
  };
}
