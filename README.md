# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency.

## Bug Description
The `useEffect` hook in `bug.js` is intended to log the current count to the console whenever the count changes. However, because the dependency array `[count]` is missing, the effect re-runs after every render, leading to an infinite loop of re-renders and log messages.

## Bug Solution
The `bugSolution.js` file provides a fix for this bug.  The missing dependency array `[count]` is added to the `useEffect` hook.  Now, the effect only runs when the value of `count` changes, preventing the infinite loop.