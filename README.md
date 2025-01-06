# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook and its dependency array.  The `useEffect` hook is designed to perform side effects after a component renders, but if the dependency array is incorrectly defined, it can lead to unexpected behavior, such as infinite loops.

## The Bug

The `bug.js` file contains a component with a `useEffect` hook that doesn't include `count` in the dependency array.  This causes the effect to run after every render, regardless of whether `count` changes, resulting in an infinite loop of rendering and console logging. 

## The Solution

The `bugSolution.js` file provides a corrected version where `count` is included in the dependency array.  This ensures that the effect only runs when `count` changes, resolving the infinite loop.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `npm start`.

Observe the console output for the original buggy component, and then compare to the corrected solution.