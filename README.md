# React useEffect Cleanup Function Not Running on Unmount

This repository demonstrates a common issue in React applications where the cleanup function within a `useEffect` hook doesn't run when the component is unmounted. This can lead to memory leaks or unexpected behavior.

## Bug Description
The cleanup function in the `useEffect` hook is designed to perform any necessary cleanup tasks before the component is unmounted, such as canceling asynchronous operations or removing event listeners.  However, in this example, the cleanup function does not execute when the component is unmounted.

## Solution
The issue is likely due to improper use of the `useEffect` hook.  Ensure the dependency array is correctly specified. In the original bug, the dependency array was missing. The dependency array should include all values that trigger the effect, in this case `count`.