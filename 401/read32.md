# Redux - Asynchronous Actions

## References

- https://redux.js.org/tutorials/fundamentals/part-6-async-logic
- https://github.com/reduxjs/redux-thunk
- https://www.digitalocean.com/community/tutorials/redux-redux-thunk

## Review, Research, and Discussion

1. How granular should your reducers be?

- as much as is needed for the application

2. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched

- Your reducer should be without side effects, simply digesting the action payload and returning a new state object. Adding listeners and dispatching actions within the reducer can lead to chained actions and other side effects.

3. Name a strategy for preventing the above

- take notes and keep track of your features

## Vocabulary

- store - A store is basically just a plain JavaScript object that allows components to share state. In a way, we can think of a store as a database. On the most fundamental level, both constructs allow us to store data in some form or another.
- combined reducers - takes an object full of slice reducer functions, and creates a function that outputs a corresponding state object with the same keys.
