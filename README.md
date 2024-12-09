# React State Not Updating After Prop Change

This repository demonstrates a common React bug where a component's state fails to update after a prop change because the `setState` call is placed in the wrong lifecycle method.  The `componentDidMount` method is used for initialization and runs only once, therefore any subsequent prop changes will not trigger a state update.

The solution involves using `componentDidUpdate` to detect prop changes and trigger the state update.

## Bug

The `bug.js` file contains the buggy React component.  The state is not updated when the `initialCount` prop changes.

## Solution

The `bugSolution.js` file contains the corrected component, using `componentDidUpdate` to handle prop changes and update the state appropriately.