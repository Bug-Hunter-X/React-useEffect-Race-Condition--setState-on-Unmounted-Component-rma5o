# React useEffect Race Condition: setState on Unmounted Component

This repository demonstrates a common React bug: a race condition in a `useEffect` hook that leads to `setState` calls on an unmounted component.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file provides a corrected version.

## Bug Description

The component fetches data asynchronously using `fetch`. If the component unmounts before the data arrives, `setData` is still called, resulting in a warning and potential errors.

## Solution

The solution uses the `mounted` state variable to check if the component is still mounted before updating state.  This prevents `setState` calls after unmounting, resolving the race condition.

## How to Run

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.