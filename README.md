# Express.js Route Handler: Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input, specifically when dealing with numeric parameters.

The `bug.js` file shows the problematic code.  The `bugSolution.js` demonstrates a corrected version with improved error handling.

## Problem

The original code attempts to parse a user ID from the request parameters and uses it to find a user in a database (simulated here with a `users` array).  However, it fails to handle the case where the `userId` is not a valid integer.

## Solution

The solution incorporates robust error handling using a `try...catch` block to manage potential errors during integer parsing. It also checks for the existence of the user before sending a response.