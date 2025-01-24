# JavaScript Closure Problem with setTimeout

This repository demonstrates a common JavaScript closure problem that arises when using `setTimeout` within a loop.  The issue stems from the way closures capture variables.

## The Bug
The `bug.js` file contains a function `myFunction` that uses `setTimeout` to log the value of `i` after a 1-second delay.  Intuitively, one might expect the output to be numbers from 0 to 9. However, due to the closure, the value of `i` is captured only *after* the loop has finished, resulting in 10 being logged 10 times.

## The Solution
The `bugSolution.js` file demonstrates a solution using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop. This ensures that each `setTimeout` callback captures its own unique value of `i`.

## How to Run
1. Clone the repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment.
3. Run each file separately to observe the different outputs.