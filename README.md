# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook: creating an infinite loop by updating state within the effect based on its previous value.

## Description
The `MyComponent` component uses `useEffect` to log the current count and increment it. This creates an infinite loop because the effect keeps re-running due to state changes caused by the increment within the effect itself. This leads to performance issues, potential crashes, and unexpected behavior.

## Solution
The solution lies in correctly understanding how `useEffect` and state updates work together. Avoid directly updating state within the effect based on its current value.  Instead, rely on external events or data changes to trigger the state updates.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and browser behavior – it shows the count incrementing infinitely.
