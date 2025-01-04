# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a server becomes unresponsive due to a long-running synchronous operation blocking the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem

The original code includes a computationally intensive loop inside the request handler.  This prevents the server from processing other requests while the loop executes, leading to unresponsiveness.  This is because Node.js is single-threaded.

## Solution

The solution involves refactoring the code to use asynchronous operations, preventing the event loop from being blocked.