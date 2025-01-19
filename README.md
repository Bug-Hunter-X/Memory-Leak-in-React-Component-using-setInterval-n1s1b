# React setInterval Memory Leak
This example demonstrates a common memory leak in React components that use `setInterval` without proper cleanup in the `useEffect` hook.  When the component unmounts, the interval continues to run, leading to wasted resources and potential performance issues.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it lacks a cleanup function within the `useEffect` hook to stop the interval when the component is unmounted.

## Solution
The `bugSolution.js` file provides the corrected version of the component.  It includes a cleanup function that uses `clearInterval` to stop the interval when the component is unmounted, preventing the memory leak.