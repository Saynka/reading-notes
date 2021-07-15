# React Native

## References

- https://reactnative.dev/docs/getting-started
- https://reactnative.dev/docs/tutorial
- https://reactnative.dev/
- https://expo.io/
- https://snack.expo.io/
- https://docs.expo.io/expokit/eject/?redirected

## Review, Research, and Discussion

1. Compare and Contrast Redux Toolkit with Redux “Ducks”

- The Redux core library is deliberately unopinionated. It lets you decide how you want to handle everything, like store setup, what your state contains, and how you want to build your reducers
- Ducks is a modular pattern that collocates actions, action types and reducers.

2. What is the principle advantage of Redux Toolkit

- makes it easier to write good Redux applications and speeds up development, by baking in our recommended best practices, providing good default behaviors, catching mistakes, and allowing you to write simpler code. Redux Toolkit is beneficial to all Redux users regardless of skill level or experience.

## Vocabulary

- redux toolkit slices - A function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state.
- namespace - Imagine we want a pattern where the children components can be composed in any order. But the children components cannot be used unless they exists in a very specific parent component.
