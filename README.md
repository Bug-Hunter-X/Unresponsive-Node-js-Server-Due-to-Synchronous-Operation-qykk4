# Unresponsive Node.js Server Due to Synchronous Operation

This repository demonstrates a common issue in Node.js applications: an unresponsive server caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the buggy code. The solution is provided in `serverSolution.js`.

## Problem

The server in `server.js` simulates a long-running task using a `while` loop.  This blocks the event loop, preventing the server from handling new requests or responding to existing ones, effectively making the server unresponsive. 

## Solution

The `serverSolution.js` demonstrates how to fix this by using asynchronous operations (Promises or async/await) or offloading the task to a worker thread or a message queue, allowing the event loop to remain responsive.