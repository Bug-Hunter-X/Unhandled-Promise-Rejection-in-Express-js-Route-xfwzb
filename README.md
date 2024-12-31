# Unhandled Promise Rejection in Express.js Route

This repository demonstrates a common error in Express.js applications:  unhandled promise rejections within route handlers.  The example code includes an asynchronous operation that can throw an error, but lacks proper error handling, resulting in a silent failure.

The `bug.js` file contains the flawed code, while `bugSolution.js` provides a corrected version with robust error handling.

## Problem

When an asynchronous operation within an Express.js route handler fails, the error is not properly caught.  This can lead to unexpected behavior and make debugging difficult.

## Solution

The solution involves using `.catch()` to handle potential errors within the promise chain.  This allows for appropriate error logging or returning error responses to the client.