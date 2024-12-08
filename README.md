# React 19 useEffect Cleanup Function Memory Leak

This repository demonstrates a common error in React 19's `useEffect` hook: forgetting to include a return statement for the cleanup function. This can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a component that uses `setInterval` within a `useEffect` hook. However, it's missing the return statement needed to clear the interval when the component unmounts.

## Solution
The `bugSolution.js` file demonstrates the correct way to use `useEffect` with `setInterval`, ensuring proper cleanup.

## How to Reproduce
1. Clone the repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `npm start`.

## Note
Always remember to include a return statement in your `useEffect` cleanup function to prevent memory leaks and ensure your components behave as expected, especially when using timers or subscriptions.