# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React: a memory leak caused by improper use of `setInterval` within the `useEffect` hook.

The `bug.js` file shows the problematic code.  The `setInterval` function is started, but there's no mechanism to stop it when the component is unmounted. This leads to a memory leak because the interval keeps running even after the component is no longer needed.

The `bugSolution.js` file provides the corrected code, demonstrating how to use the cleanup function in `useEffect` to properly clear the interval before unmounting, thus preventing the memory leak.