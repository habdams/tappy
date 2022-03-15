# Responding to Events
*React lets you add event handlers to your jsx.*

1. Different ways to write event handlers.
2. How to pass event handlng logic from a parent component.
3. How events propagate and how to stop them.

1.
Event handlers: 
- usually defined inside your components.
- by convention, name them handle<followed by the event handled>
- Alternatively you can define them inside the JSX.

Note:
- Always pass in a function, not call a function.
- Function called fires at every render of a component.
**e.g**
```
onPress = {handleButtonPress} - *good*
```
```
onPress = {handleButtonPress()} - *caution- fires on component render*
```

Event handlers have access to the components props as they are declared inside a component.

- By convention event handler props start with on<followed by capital letter> e.g: [onPress]

## Event propagation
- All events propagates in React except **onScroll**.

###
```stopPropagation()```
- stops an event bubble/propagation: stops the event handlers attached to the tags above from firing.

```preventDefault()```
-prevents defaults browsers behaviour/actions for few events that have it.