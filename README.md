# Unnecessary Re-renders in React useEffect Hook

This example demonstrates a common React bug involving the `useEffect` hook. The `useEffect` hook, without a proper dependency array, causes unnecessary re-renders and can lead to performance degradation. The solution showcases how to correctly use the dependency array to optimize performance.

## Bug
The `useEffect` hook in the provided code runs after every render, even if the value of `count` hasn't changed. This leads to excessive console logs and unnecessary work.

## Solution
Adding `[count]` as the dependency array to the `useEffect` hook ensures that the effect runs only when the value of `count` changes, fixing the unnecessary re-renders.