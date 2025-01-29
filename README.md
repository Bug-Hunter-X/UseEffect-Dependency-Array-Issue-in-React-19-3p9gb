# React 19 useEffect Hook Dependency Issue

This repository demonstrates a common issue with the `useEffect` hook in React 19: incorrect or missing dependency arrays.  The `bug.js` file shows an example where the dependency array is missing `count`, leading to an infinite loop and unexpected behavior. The `bugSolution.js` file provides the correct implementation.

## Problem

The `useEffect` hook without a correctly defined dependency array may lead to unexpected behavior because the effect function will run after every render. When `count` is missing from the dependency array, the effect runs indefinitely.

## Solution

Add the `count` variable to the dependency array, making sure that the effect only runs when `count` changes.