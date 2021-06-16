# Login and <uth

## Refrences

- https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more
- https://www.npmjs.com/package/react-cookies
- https://www.npmjs.com/package/react-cookie

## Review, Research, and Discussion

1. Why is the Context API useful?

- The React Context API is a way for a React app to effectively produce global variables that can be passed around. This is the alternative to "prop drilling" or moving props from grandparent to child to parent, and so on. Context is also touted as an easier, lighter approach to state management using Redux.

2. Can a component outside of a provider get its context?

- you have to wrap the components in with other stuff

3. What are some common use cases for using the Context API?

- Theming — Pass down app theme. i18n — Pass down translation messages. Authentication — Pass down current authenticated user.

4. Describe “Context Hell”

- usual when jQuery was used for everything, the React Context hell is the nasty code you get taking advantage of the React Context API.

## Vocabulary

- global state - managing state in multiple components that are not directly connected.
- global context - Context provides a way to pass data through the component tree without having to pass props down manually at every level, managing state in multiple components that are not directly connected.
- provider - component makes the Redux store available to any nested components that need to access the Redux store. Since any React component in a React Redux app can be connected to the store, most applications will render a <Provider> at the top level, with the entire app's component tree inside of it.
- consumer - A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component. Requires a function as a child. The function receives the current context value and returns a React node.
