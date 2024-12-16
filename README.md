## Unhandled Error in Express.js Route Parameter Parsing

This repository demonstrates a common error in Express.js route handlers:  lack of error handling when parsing route parameters. The `bug.js` file shows a route that attempts to parse a user ID from the request parameters without proper validation or error handling. This can lead to unexpected errors and crashes.  The `bugSolution.js` file provides a corrected version with appropriate error handling.

### Problem:
The original code fails to handle cases where the `:id` parameter is not a valid integer.  Attempting to parse a non-numeric string as an integer will cause a runtime error.

### Solution:
The solution includes checks to ensure the `id` parameter is a valid number before attempting to parse it. If it's not a number or if the user is not found, appropriate error responses are returned.