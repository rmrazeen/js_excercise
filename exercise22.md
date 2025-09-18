# JavaScript Exercise 2 (Hard)

## Problem: Implement a `throttle` function

Create a `throttle` function that takes a function `func` and a `delay` as arguments. The `throttle` function should return a new function that, when invoked, will execute `func` at most once every `delay` milliseconds.

### Example Usage:

```javascript
function logScroll(event) {
  console.log("Scrolled!", event);
}

const throttledScroll = throttle(logScroll, 200);

window.addEventListener("scroll", throttledScroll);
// logScroll will be called at most once every 200ms during scrolling
```

### Solution Structure:

```javascript
function throttle(func, delay) {
  let inThrottle, lastFn, lastTime;
  return function() {
    const context = this,
      args = arguments;
    if (!inThrottle) {
      func.apply(context, args);
      lastTime = Date.now();
      inThrottle = true;
    } else {
      clearTimeout(lastFn);
      lastFn = setTimeout(function() {
        if (Date.now() - lastTime >= delay) {
          func.apply(context, args);
          lastTime = Date.now();
        }
      }, Math.max(delay - (Date.now() - lastTime), 0));
    }
  };
}
