# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, this example shows a route that fetches a user by ID, but fails to handle cases where the ID is not a valid number.

## Bug

The `bug.js` file contains the buggy code.  It attempts to parse the user ID as an integer directly without checking its type, resulting in a potential `NaN` error or unexpected behavior if the ID is not a number.

## Solution

The `bugSolution.js` file shows the corrected code. It includes error handling to check if the user ID is a valid number before attempting to parse it and find the user.  A 400 Bad Request is returned if the ID is invalid.