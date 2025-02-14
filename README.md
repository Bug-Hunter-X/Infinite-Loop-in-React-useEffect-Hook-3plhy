# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## Bug Description
The `MyComponent` component uses `useEffect` to log the current `count` value.  However, the `setCount` function call inside the effect modifies `count`, which triggers another render and another execution of the effect, creating an infinite loop. 

## Solution
The solution involves adding the `count` variable to the dependency array in the `useEffect` hook. This ensures the effect only runs when `count` changes. 