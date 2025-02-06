# Express.js: Handling Large JSON Payloads
This repository demonstrates a common issue in Express.js applications where large JSON payloads are not parsed correctly, leading to errors.  The `bug.js` file contains the erroneous code, and `bugSolution.js` provides the solution.

## Problem
The original code uses `express.json()` without specifying limits, causing the server to fail when processing large JSON inputs.  This often manifests as a request body parsing error, potentially crashing the server.

## Solution
The solution involves setting the `limit` option in `express.json()` to handle larger JSON payloads.  The `limit` can be set to a specific number of bytes or using human-readable units like '10mb'.  This ensures that the server can parse larger JSON objects without failure.

## How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install express`
4. Run `node bug.js` (to see the error)
5. Run `node bugSolution.js` (to see the working solution)
