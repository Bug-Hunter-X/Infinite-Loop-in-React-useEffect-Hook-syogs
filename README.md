# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The example shows an infinite loop caused by missing dependencies in the useEffect's dependency array.  This leads to an infinite re-rendering cycle, resulting in performance issues and potential application crashes.  The solution demonstrates how to fix the issue by correctly specifying dependencies to control when the effect runs.

## Bug

The `bug.js` file contains the buggy code. The `useEffect` hook's dependency array is missing, which causes the function within `useEffect` to be re-executed after every render, even when the `count` is updated within that function itself.

## Solution

The `bugSolution.js` file provides a corrected version.  The dependency array `[count]` is added to the `useEffect` hook.  This ensures that the effect only runs when the value of `count` changes.