# React useEffect Hook Missing Cleanup Function

This repository demonstrates a common error in React's `useEffect` hook: missing a cleanup function.  The provided `bug.js` file shows an example of this, and `bugSolution.js` provides the corrected code.

## Problem

The `useEffect` hook in `bug.js` has a missing return statement.  Specifically the return statement should contain a cleanup function that will be executed before the component unmounts or when the effect runs again.  Without this cleanup function, resources may not be properly released, leading to memory leaks, especially if there are subscriptions to external resources, such as event listeners or timers.

## Solution

The `bugSolution.js` file corrects the issue by adding a proper return statement that returns a cleanup function. This function handles releasing any resources acquired by the effect.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory containing `bug.js` and run the React application.
3. Observe the console logs to see the missing cleanup function behavior. 
4. Replace `bug.js` with `bugSolution.js` and re-run the application to observe the corrected behavior.
