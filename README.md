# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common error involving the `useEffect` hook in React 19 that can lead to an infinite loop and excessive console logging.  The issue stems from using `useEffect` without specifying a dependency array, causing it to execute after every render.

## Bug Description

The `bug.js` file contains a React component with a `useEffect` hook that logs the current count to the console.  Because the dependency array is missing, the effect runs on every render, leading to an infinite loop and repeated console messages.

## Solution

The `bugSolution.js` file demonstrates the correct usage of `useEffect`. By including `[count]` as the dependency array, the effect only runs when the `count` variable changes.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server. 
4. Observe the behavior in your browser's console.

## Lessons Learned

Always specify a dependency array in `useEffect` to control when the effect runs.  Omitting it can lead to unexpected behavior and performance issues.