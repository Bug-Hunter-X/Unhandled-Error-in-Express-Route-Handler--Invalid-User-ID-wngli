# Unhandled Error in Express Route Handler: Invalid User ID

This repository demonstrates a common error in Express.js route handlers: lack of error handling for invalid input. The `bug.js` file contains the erroneous code, which fails to properly handle cases where the user ID is not a number.  The `bugSolution.js` file provides a corrected version.

## Bug
The original code attempts to parse the request parameter `id` as an integer using `parseInt()` without first validating that it is a number.  If a non-numeric ID is passed, `parseInt()` will return `NaN`, causing the `find()` method to fail silently or potentially throw an error, leading to an unexpected response or application crash.

## Solution
The solution adds input validation to check if `userId` can be parsed as an integer before proceeding.  If the parsing fails, a suitable error message is returned to the client.