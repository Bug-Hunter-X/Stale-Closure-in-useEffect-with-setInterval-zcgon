# Stale Closure in useEffect with setInterval
This repository demonstrates a common error in React when using `setInterval` within a `useEffect` hook. The issue arises from a stale closure, where the callback function references an outdated value of `count`.

## Bug Description
The `MyComponent` attempts to increment a counter every second using `setInterval`. However, the callback function within `setInterval` uses the initial value of `count` captured during the initial render instead of updating with the latest state value.