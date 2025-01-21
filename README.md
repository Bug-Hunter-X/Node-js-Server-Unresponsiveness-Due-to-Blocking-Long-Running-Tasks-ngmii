# Node.js Server Unresponsiveness Due to Blocking Long-Running Tasks

This repository demonstrates a common Node.js issue: server unresponsiveness caused by long-running operations that block the event loop.  The `server.js` file contains code that simulates a 5-second delay, making the server unresponsive during that time.  The solution (`serverSolution.js`) showcases how to address this using asynchronous programming with promises or async/await.

## How to Reproduce

1. Clone this repository.
2. Run `node server.js`.
3. Attempt to make a request to `http://localhost:3000`. You'll notice the request hangs for 5 seconds.

## Solution

The solution in `serverSolution.js` demonstrates using async/await to prevent blocking the event loop.  This allows Node.js to handle other requests concurrently even while a long-running task is in progress.  This technique is crucial for building scalable and responsive Node.js applications.