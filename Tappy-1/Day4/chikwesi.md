# Day 3
**Focus** ==[Render and Commit](https://beta.reactjs.org/learn/render-and-commit)


## Rendering
Rending is made up of three stages
1. Trigger
2. Render
2. Commit

### Trigger

There are 2 instances trigger rendering.
1. During intial rendering
```
React.render(
    <ReactComponent/>,
    document.getElementById('root')
)
```
2. When component state changes.

### Render

1. On intial render react calls the root component
2. During a re-render react calls the function components whose state update triggered the re-render. If the component returns another component and that also returns another component and so on, all those components a re-rendered. this process is recursive.

> During renders react calculates the difference between the components states and the DOM. This calculation is used in the commit phase

Rendering must be Pure
1. Same inputs must give the same output
2. it should not modify objects or variables that existed before rendering.

### Commit
1. During intial render react calls `appendChild()`
2. During re-renders react calculates the difference between the DOM and the rendered output and peforms the minimal operations so the DOM matches the latest rendered output


> Note: Rendering and committing stages are different.
In the commit stage the browser paints the screen.

summary
1. A component can have multiple useState declarations.
2. If state depends on one another is better to set the state as a object

