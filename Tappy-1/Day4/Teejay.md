# State: A Components Memory

### Problem
Local variables don't persist between renders
- Rect renders the component a second timr from scratch and doesn't consider any canges to local variables.
- Changes to local variables won't trigger renders.

### Need
- Retain data
- Trigger render with new data

### Solution
## useState

- A state variable to retain the data between renders.
- A state setter function to update the variable and trigger react to render the component again.

**useState** and other functions starting with 'use' are called hooks, special fnctions that allow you perform certain operations while the coponent is rendering.

"Only available when React is rendering"

### How does setState know which state to return?

- Hook rely on a stable call order on every render of the same component.

### What does it mean for state to be local

- State is local to the component instance on the screen.

```
    <PictureComp /> // The state here is isolated from 
    <PictureComp /> // the state here.
```