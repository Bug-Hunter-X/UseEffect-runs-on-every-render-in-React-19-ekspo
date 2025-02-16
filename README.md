# React 19 useEffect Bug

This repository demonstrates a bug where `useEffect` in React 19 runs on every render, even when a dependency array is provided.  This behavior is unexpected and can lead to performance issues.

## Bug Description

The `useEffect` hook is designed to run only when its dependencies change. However, in this specific scenario, the `useEffect` hook inside `MyComponent` runs on every render, regardless of whether the `count` state variable has changed.

## Solution

The issue arises from an incorrect dependency array. To fix this bug, ensure that all values used inside the useEffect that are not defined within the function itself are declared in the dependency array.