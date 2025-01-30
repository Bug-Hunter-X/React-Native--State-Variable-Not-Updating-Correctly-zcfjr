# React Native: State Variable Not Updating Correctly

This repository demonstrates a common error in React Native where a state variable within a function component fails to update correctly, leading to stale data. The issue occurs when directly modifying the state variable instead of utilizing the setter function provided by the `useState` hook.

## Problem

The `bug.js` file showcases the problematic code. The `incrementCount` function attempts to increment the state variable `count` directly, causing the state update to be ignored and resulting in the displayed count remaining unchanged despite the button press.

## Solution

The corrected code is found in `bugSolution.js`. It demonstrates how to correctly update the state variable using the setter function (`setCount`) provided by `useState`. This ensures that the component re-renders with the updated state value.

## How to reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npx react-native run-android` or `npx react-native run-ios` to run the app on an emulator or physical device.
5. Observe that the count in `bug.js` does not increment, whereas in `bugSolution.js`, it increments correctly.