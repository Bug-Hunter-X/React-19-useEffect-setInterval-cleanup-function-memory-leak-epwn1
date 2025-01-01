# React 19 useEffect setInterval Cleanup Function
This repository demonstrates a common error when using the `useEffect` hook with `setInterval` in React 19.  Forgetting to include a cleanup function in the `useEffect` hook can lead to memory leaks as the interval continues to run even after the component unmounts.

## Bug Description
The `bug.js` file contains a component that uses `useEffect` to increment a counter every second using `setInterval`. However, it lacks a cleanup function to clear the interval when the component unmounts. This results in the interval continuing to run, potentially causing a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct usage of `useEffect` with `setInterval`, including a cleanup function to prevent memory leaks. The cleanup function uses `clearInterval` to stop the interval when the component unmounts.

## How to reproduce
1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install`.
4. Run `npm start`.
5. Observe the counter incrementing every second.
6. Unmount the component and observe that the interval continues to run (in the buggy version).

## How to fix
Refer to the corrected code in `bugSolution.js` to see how to properly implement cleanup within `useEffect` when dealing with `setInterval` or similar asynchronous operations.