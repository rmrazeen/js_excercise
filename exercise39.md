# Exercise 10: Asynchronous JavaScript (Promises and Async/Await)

**Goal**: Understand and implement asynchronous operations using Promises and `async/await`.

```js
// Simulate an asynchronous operation
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const success = true; // Simulate success or failure
      if (success) {
        resolve("Data fetched successfully!");
      } else {
        reject("Failed to fetch data.");
      }
    }, 2000); // Simulate a 2-second delay
  });
}

// Using Promises
console.log("Fetching data with Promises...");
fetchData()
  .then(data => {
    console.log("Promise success:", data);
  })
  .catch(error => {
    console.error("Promise error:", error);
  });

// Using Async/Await
async function getData() {
  console.log("\nFetching data with Async/Await...");
  try {
    const data = await fetchData();
    console.log("Async/Await success:", data);
  } catch (error) {
    console.error("Async/Await error:", error);
  }
}
getData();

// Another example with async/await and multiple awaits
async function processData() {
  try {
    console.log("\nProcessing data...");
    const result1 = await new Promise(resolve => setTimeout(() => resolve("Step 1 complete"), 1000));
    console.log(result1);
    const result2 = await new Promise(resolve => setTimeout(() => resolve("Step 2 complete"), 1000));
    console.log(result2);
    console.log("All steps complete!");
  } catch (error) {
    console.error("Processing error:", error);
  }
}
processData();
```

**What to learn**: Asynchronous programming concepts, Promises (`.then()`, `.catch()`), `async/await` syntax, error handling in async code.
