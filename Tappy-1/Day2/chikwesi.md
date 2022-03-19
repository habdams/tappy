# Day 2
**Focus** ==[Responding To Events](https://beta.reactjs.org/learn/responding-to-events)

You can add event handlers to jsx tags by passing the handle as a props to the appropraite jsx tag.

```
function eventHander(){
    //do something
}
<button onclick={eventHandler}/>
```


> It is convention to name event handers as event followed by handler. e.g clickHander() mouseEnterHandler()

when passing event handlers it is important to pass the reference for the function and not call the function

**#Correct**
```
function eventHander(){
    //do something
}
<button onclick={eventHandler}/>
```

**#Wrong**

```
function eventHander(){
    //do something
}
<button onclick={eventHandler()}>
```


You can also define inline handlers.

```
<button onclick={function eventHander(){
    //do something
}}/>
```

```
<button onclick={() => doSomething()}/>
```

inline handler it is important to pass the function and not call it

**#wrong**
```
<button onclick={doSomething()}/>
```
## Summary

1. Handlers can be passed the from a parent component to a child component using props.

2. Props defined in a component are assemeble in even handler functions.
3. A component can have a custom prop name that can be used to distuigish different kinds of event.
> By convention custom event prop names should start  with 'on' followed by Capital letters. e.g onPlayMovie
4. `event.stopPropagation` stops the event from bubbling up the dom tree to parent element.
In react every event apart from the pageScroll event propagates
5. `event.prevendDefault` prevents browser built in behaviours for events. e.g Refreshing a from after clickint the submit button.

