# Context API

## Refrences

- https://reactjs.org/docs/context.html
- https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b
- https://github.com/diegohaz/awesome-react-context

## Review, Research, and Discussion

1. Describe use cases for useMemo() and useReducer()

- useMemo() - is a React hook that memorizes the output of a function. That is it. useMemo accepts two arguments: a function and a list of dependencies. useMemo will call the function and return its return value. ... If they have changed, useMemo will call the provided function again and repeat the process.
- useReducer() - is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

2. Why do custom hooks need the use prefix?

- it's just like a normal function. Its name should always start with use so that you can tell at a glance that the rules of Hooks apply to it. Now let's see how we can use our custom Hook.

3. What do custom hooks usually do?

- Custom hooks allow us to have cleaner functional components, remove logic from the UI layer, and prevent code duplication by bringing common use cases to reusable hooks.

4. Using any list of custom hooks, research and name one that you think will be useful in your applications

- component from a chat application that displays a message indicating whether a friend is online or offline:

5. Describe how a hook that fetches API data might work

- First, we're going to import stuff we're going to use and create a function. The next step is to add a useState hook and to define the name of the state - in our case, that's data. Then, we define the function we'll use later on to update the state - setData.

## Vocabulary

- reducer - A reducer is a pure function that takes state and action as parameters and returns the new state. There may be many reducers managing parts of the root state. We can combine them together with combineReducers() utility function and create the root reducer.
