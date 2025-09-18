# Medium Exercise 9: Implement a Queue

**Goal**: Implement a basic Queue data structure in JavaScript with `enqueue` (add to back) and `dequeue` (remove from front) methods.

```js
class Queue {
  constructor() {
    this.items = [];
  }

  enqueue(element) {
    this.items.push(element);
  }

  dequeue() {
    if (this.isEmpty()) {
      return "Underflow"; // Queue is empty
    }
    return this.items.shift();
  }

  front() {
    if (this.isEmpty()) {
      return "No elements in Queue";
    }
    return this.items[0];
  }

  isEmpty() {
    return this.items.length === 0;
  }

  size() {
    return this.items.length;
  }

  printQueue() {
    let str = "";
    for (let i = 0; i < this.items.length; i++)
      str += this.items[i] + " ";
    return str;
  }
}

const queue = new Queue();
console.log("Is queue empty?", queue.isEmpty()); // Expected: true

queue.enqueue(10);
queue.enqueue(20);
queue.enqueue(30);
console.log("Queue after enqueuing:", queue.printQueue()); // Expected: "10 20 30 "
console.log("Front element:", queue.front()); // Expected: 10

console.log("Dequeued element:", queue.dequeue()); // Expected: 10
console.log("Queue after dequeuing:", queue.printQueue()); // Expected: "20 30 "
console.log("Queue size:", queue.size()); // Expected: 2
```

**What to learn**: Class definition, constructor, array methods (`push`, `shift`), basic data structure implementation.
