# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook:  omitting a dependency from the dependency array, leading to an infinite loop. The counter component increments rapidly, freezing the browser tab.

## Bug Description

The `useEffect` hook is used to set up a timer that updates a counter.  However, the `count` variable is missing from the dependency array. This causes the effect to run continuously, resulting in an infinite loop and rapid counter updates.

## Solution

Adding `count` to the dependency array fixes the issue.  Now, the effect will only run when the `count` value changes.