# Node.js Server Hang on Long Requests

This repository demonstrates a common issue in Node.js servers where long-running operations can block the event loop, making the server unresponsive.  The example simulates a 5-second delay, causing the server to appear to hang during that time. The solution provides an improved approach using asynchronous operations.

## Bug
The `bug.js` file contains the buggy code.  It creates an HTTP server that simulates a long-running operation (5-second delay) within the request handler.  During this delay, the server becomes unresponsive to other requests.

## Solution
The `bugSolution.js` file demonstrates how to avoid blocking the event loop by handling long-running operations asynchronously.