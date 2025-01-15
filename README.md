# Node.js Unhandled Exception Bug

This repository demonstrates a common error in Node.js where unhandled exceptions within an HTTP server's request handler can lead to unexpected server crashes. The `bug.js` file contains the problematic code, while `bugSolution.js` provides a corrected version that gracefully handles errors.

## Bug Description

The original code lacks proper error handling.  If an exception occurs during request processing, the server terminates abruptly without providing a meaningful response to the client. This makes the server unreliable and difficult to debug.

## Solution

The solution implements a `try...catch` block within the request handler to catch potential exceptions.  If an error occurs, it logs the error and sends a suitable error response to the client, preventing the server from crashing.