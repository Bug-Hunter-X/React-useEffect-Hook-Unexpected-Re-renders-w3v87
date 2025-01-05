# React useEffect Hook Unexpected Re-renders

This repository demonstrates a common React error involving the `useEffect` hook. The example shows how a missing or incorrect dependency array can lead to unexpected re-renders and, in some cases, an infinite loop.

## Bug Description

The provided `MyComponent` uses `useEffect` without specifying any dependencies. This means the effect runs after every render, creating an infinite loop because updating the state triggers a re-render, and thus triggers the effect again.

## Solution

The solution involves correctly specifying the dependencies in the dependency array of the `useEffect`.  In this example, since the effect does not depend on any props or state values, an empty array `[]` ensures the effect runs only once after the initial render.