# Day 3
**Focus** ==[State: A Components Memory](https://beta.reactjs.org/learn/state-a-components-memory)

State is a components memory:
 1. It allows you to remember values between rerenders.
 2. ***trigger*** a re-render when the value changes.

 ## Hooks

> Hooks are special functions that start with use, they allows us to 'Hook into' react features e.g state

Hooks are ***uncondional declarations*** and therefore the must be written at the top level of your component. Not inside conditionals or inner functions. Just like `import ` statements.

The `useState` hooks provides two things: 

1. provides a state variable that is retain data between re-renders
2. It provides a functio to update the state variable and trigger a re-render


```
const [variable, setVarible] = useState(initialValue)
```

> It is convention the name the update function stating with set and then the variable name*

A component can have multiple useState declarations.

## State is private

>State is local to a component instance on a screen.

A component does not know anything about the state of another component. Even if it is the same component render twice

## Summary

1. A component can have multiple useState declarations.
2. If state depends on one another is better to set the state as a object

