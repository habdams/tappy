# Rnder and Commit

Components must be rendered before they are displayed on screen

### The Process Of Requesting and Serving UI
- Triggering render
- Rendering the component
- Commiting to the DOM

### Reasons for a component to render(Triggering)
- its initial render
----- this is done by calling ReactDOM.render() with the root component(e.g <App />) and the target DOM node(document.getElementById('root')).
- its state has been changed
## React renders your component(Rendering)
- on initial render, React calls the root component
- subsequent renders - React the funtion component whose state update triggers the render
`The process is recursive - If the updated component returns some other component, React will render the component next and so on` 

## React commits changes to DOM(Commiting)

Afte rendering, React will modify the DOM

- For initial render, React will use appendChild() DOM API to insert the DOM nodes it created on the screen.
- For re-renders, React will apply the minimal necessary operations (calculated while rendering!) to make the DOM match the latest rendering output.

`React only changes the DOM nodes if there's a difference between renders`