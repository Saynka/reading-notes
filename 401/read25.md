# Hooks API

## refrences

- https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889
- https://reactjs.org/docs/hooks-state.html
- https://reactjs.org/docs/hooks-overview.html
- https://reactjs.org/docs/hooks-reference.html
- https://reactjs.org/docs/hooks-effect.html

## Review, Research, and Discussion

1. Why do we not need more .html pages in a multi-page React app?

- Because React is not designed to develop multi-page websites. So, we need to create multiple routes to handle multiple views.

2. If we wanted a component to show up on every page, where would we put it and why?

- Outside the <BrowserRouter/> - putting it on the outside will render no matter what route your on

3. What does props.children contain?

- the property of the wrapper

## Vocabulary

- Composition - is a development pattern based on React's original component model where we build components from other components using explicit defined props or the implicit children prop.
- Children / Child Components - allow you to pass components as data to other components, just like any other prop you use. ... The special thing about children is that React provides support through its ReactElement API and JSX. XML children translate perfectly to React children!
- Hash Routing - This is a solution to React Router's issue of not scrolling to #hash-fragments when using the <Link> component to navigate. When you click on a link created with react-router-hash-link it will scroll to the element on the page with the id that matches the #hash-fragment in the link.
- Link Routing - use the <NavLink /> component by react-router-dom . The NavLink component provides a declarative way to navigate around the application. It is similar to the Link component, except it can apply an active style to the link if it is active.
