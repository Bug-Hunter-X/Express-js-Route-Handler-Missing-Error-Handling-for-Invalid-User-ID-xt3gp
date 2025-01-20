# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. Specifically, the example shows a route that retrieves a user by ID, but fails to handle cases where the ID is not a valid number.

## Bug

The `bug.js` file contains an Express.js route handler that fetches a user from an array of users using the ID provided in the request parameters. However, it lacks error handling for situations where the provided `userId` is not a number, leading to unexpected behavior or potential crashes.

## Solution

The `bugSolution.js` file provides the corrected route handler. It includes error handling using `isNaN` to check if the `userId` is a valid number. If not, it sends a 400 Bad Request response, providing informative feedback to the client.  If the user is not found, it sends a 404 Not Found response.