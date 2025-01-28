# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes the component to re-render infinitely, leading to a stack overflow error.  The solution involves correctly specifying dependencies in the `useEffect` hook.

## Bug Description

The provided code demonstrates an infinite loop within a React component's `useEffect` hook. Because the `useEffect` hook doesn't have a dependency array, it runs after every render, causing a loop. This loop is due to the `setCount` function being used in `useEffect` causing a re-render, triggering the `useEffect` again.