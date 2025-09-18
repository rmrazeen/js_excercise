# JavaScript Exercise 3 (Hard)

## Problem: Implement a custom `Promise.all`

Create a function `customPromiseAll` that mimics the behavior of `Promise.all`. It should take an array of promises as input and return a new promise. This new promise should resolve with an array of results from the input promises, in the same order, once all of them have resolved. If any of the input promises reject, the `customPromiseAll` promise should reject with the reason of the first promise that rejected.

### Example Usage:

```javascript
const promise1 = Promise.resolve(3);
const promise2 = 42;
const promise3 = new Promise((resolve, reject) => {
  setTimeout(resolve, 100, 'foo');
});

customPromiseAll([promise1, promise2, promise3]).then((values) => {
  console.log(values); // Expected: [3, 42, "foo"]
});

const promise4 = new Promise((resolve, reject) => setTimeout(reject, 200, 'Error!'));
customPromiseAll([promise1, promise4]).catch((error) => {
  console.error(error); // Expected: "Error!"
});
```

### Solution Structure:

```javascript
function customPromiseAll(promises) {
  return new Promise((resolve, reject) => {
    const results = [];
    let completed = 0;
    const total = promises.length;

    if (total === 0) {
      resolve([]);
      return;
    }

    promises.forEach((promise, index) => {
      Promise.resolve(promise)
        .then((value) => {
          results[index] = value;
          completed++;
          if (completed === total) {
            resolve(results);
          }
        })
        .catch((error) => {
          reject(error);
        });
    });
  });
}
