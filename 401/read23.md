# Routing

## refrences

- https://blog.pshrmn.com/simple-react-router-v4-tutorial/
- https://reactrouter.com/web/api
- https://www.npmjs.com/package/react-if
- https://testing-library.com/docs/queries/about/
- https://www.w3.org/TR/html-aria/

## Review, Research, and Discussion

1. Do child components have direct access to props/state from the parent?

- there is no way to pass props from a child component to a parent component. However, we can always pass around functions from the parent to child component. The child component can then make use of these functions. The function can then update the state in a parent component,

2. When a component “wraps” another component, how does the child component’s output get rendered?

- The function will accept as one of its arguments a child component that receives ... props of the container, along with a new prop, data , which it uses to render its output. ... More crucially, if you apply another HOC to EnhancedComponent that also ... render() { // Wraps the input component in a container, without mutating it.

3. Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?

- yes

4. What trick can a parent use to share all props with it’s children

- props.cheldren

## Vocabulary

- props.children - it is used to display whatever you include between the opening and closing tags when invoking a component.
- composition - is a development pattern based on React's original component model where we build components from other components using explicit defined props or the implicit children prop.
