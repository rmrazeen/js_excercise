# JavaScript Exercise 10 (Hard)

## Problem: Implement a simple `useState` hook

Create a function `createUseState` that mimics the behavior of React's `useState` hook. It should return a function that, when called, returns an array containing the current state value and a function to update it. The update function should accept a new value or a function that takes the previous state and returns the new state.

### Example Usage:

```javascript
const useState = createUseState();

function Counter() {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  const decrement = () => {
    setCount((prevCount) => prevCount - 1);
  };

  console.log("Current count:", count);
  return { count, increment, decrement };
}

const { count: c1, increment: inc1, decrement: dec1 } = Counter(); // Initial render
inc1();
const { count: c2, increment: inc2, decrement: dec2 } = Counter(); // Re-render
dec2();
const { count: c3 } = Counter(); // Re-render

// Expected output:
// Current count: 0
// Current count: 1
// Current count: 0
```

### Solution Structure:

```javascript
function createUseState() {
  let state;
  let firstCall = true;

  return function useState(initialValue) {
    if (firstCall) {
      state = initialValue;
      firstCall = false;
    }

    const setState = (newValue) => {
      if (typeof newValue === 'function') {
        state = newValue(state);
      } else {
        state = newValue;
      }
      // In a real React app, this would trigger a re-render.
      // For this exercise, we just update the state.
    };

    return [state, setState];
  };
}
