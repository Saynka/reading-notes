# Custom Hooks

## Refrences

- https://www.telerik.com/kendo-react-ui/react-hooks-guide/#toc-custom-react-hooks
- https://dev.to/vinodchauhan7/react-hooks-with-async-await-1n9g
- https://reactjs.org/docs/hooks-reference.html#usereducer
- https://reactjs.org/docs/hooks-custom.html
- https://usehooks.com/
- https://github.com/rehooks/awesome-react-hooks
- https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d

## Review, Research, and Discussion

1. What does a component’s lifecycle refer to?

- lifecycle of a component can be defined as the series of methods that are invoked in different stages of the component's existence.

2. Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect

- useCallback will help in avoiding regeneration of functions when the functional component re-renders. However there isn't much of a performance difference caused by recreation of functions. You are specifying a function as a dependency to useEffect

3. Why are functional components preferred over class components?

- Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks. You end up with less code. They help you to use best practices.

4. What is wrong with the following code?

- syntax from the looks of it

## Vocabulary

- state hook - A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.
- effect hook - useEffect is a hook for encapsulating code that has 'side effects,' and is like a combination of componentDidMount , componentDidUpdate , and componentWillUnmount . Previously, functional components didn't have access to the component life cycle, but with useEffect you can tap into it.
- reducer hook - useReducer is one of a handful of React hooks that shipped in React 16.7. 0. It accepts a reducer function with the application initial state, returns the current application state, then dispatches a function.
