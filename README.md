# Express.js Route Handler Bug

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. The `bug.js` file contains the buggy code, which attempts to parse a user ID from the request parameters but does not handle the case where the ID is not a valid integer.  This can result in unexpected behavior or crashes. The `bugSolution.js` file shows how to fix this by adding appropriate error handling.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `node bug.js` and try accessing a route with an invalid ID (e.g., `/users/abc`).
4. Observe the error.
5. Run `node bugSolution.js` and try the same request.  The error should be handled gracefully.

## Solution

The solution involves checking if `parseInt(userId)` successfully parses an integer and handling the case where it doesn't.