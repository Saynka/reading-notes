# Redux - Additional Topics

## References

- https://redux-toolkit.js.org/
- https://redux-toolkit.js.org/tutorials/overview
- https://mobx.js.org/getting-started.html
- https://hookstate.js.org/

## Review, Research, and Discussion

1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?

- The most 'redux-like' way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount ) of a Higher Order Component that wraps your app.

2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

- You can manage asynchronous actions in Redux with Thunk, or you could ... that you dispatch the action that starts the asynchronous task. ... That said, you may be tempted to support asynchronous actions by modifying their reducers,

## Vocabulary

- middleware - software that acts as a bridge between an operating system or database and applications, especially on a network.
- thunk - Thunk middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action,
