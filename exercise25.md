# JavaScript Exercise 5 (Hard)

## Problem: Implement a custom `EventEmitter`

Create a class `EventEmitter` that allows for subscribing to and emitting events. It should have `on`, `off`, and `emit` methods.

- `on(eventName, listener)`: Registers a `listener` function to be called when `eventName` is emitted.
- `off(eventName, listener)`: Unregisters a `listener` function for `eventName`.
- `emit(eventName, ...args)`: Calls all registered listeners for `eventName` with `...args`.

### Example Usage:

```javascript
const emitter = new EventEmitter();

function greet(name) {
  console.log(`Hello, ${name}!`);
}

function farewell(name) {
  console.log(`Goodbye, ${name}!`);
}

emitter.on('greet', greet);
emitter.on('greet', farewell); // Can have multiple listeners for the same event

emitter.emit('greet', 'Alice'); // Expected: "Hello, Alice!" and "Goodbye, Alice!"

emitter.off('greet', greet);
emitter.emit('greet', 'Bob'); // Expected: "Goodbye, Bob!" (greet listener removed)

emitter.off('greet', farewell);
emitter.emit('greet', 'Charlie'); // No output (all listeners removed)
```

### Solution Structure:

```javascript
class EventEmitter {
  constructor() {
    this.events = {};
  }

  on(eventName, listener) {
    if (!this.events[eventName]) {
      this.events[eventName] = [];
    }
    this.events[eventName].push(listener);
  }

  off(eventName, listener) {
    if (!this.events[eventName]) {
      return;
    }
    this.events[eventName] = this.events[eventName].filter(
      (l) => l !== listener
    );
  }

  emit(eventName, ...args) {
    if (!this.events[eventName]) {
      return;
    }
    this.events[eventName].forEach((listener) => {
      listener(...args);
    });
  }
}
