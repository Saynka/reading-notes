# Combined Reducers

## References

- https://www.youtube.com/watch?v=gBER4Or86hE
- https://redux.js.org/recipes/structuring-reducers/using-combinereducers/
- https://redux.js.org/api/combinereducers/

## Review, Research, and Discussion

1. Why choose Redux instead of the Context API for global state?

- Context API: Resourceful and ideal for small applications where state changes are minimal
- Redux: Perfect for larger applications where there are high-frequency state updates

2. What is the purpose of a reducer?

- A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently.

3. What does an action contain?

- Actions are the only source of information for the store as per Redux official documentation. It carries a payload of information from your application to store. As discussed earlier, actions are plain JavaScript object that must have a type attribute to indicate the type of action performed.

4. Why do we need to copy the state in a reducer?

- redux only requires our reducers to stay pure. If the new state is different, the reducer must create new object, and making a copy is a way to describe the unchanged part

## Vocabulary

- immutable state - React state should be treated as immutable. ... This means a manual state mutation may be overridden when setState is processed. If you declare a shouldComponentUpdate method, you can't use a === equality check inside because the object reference will not change.
- time travel in redux - Time travel debugging refers to the ability step forward and backward through the state of you application, empowering the developer understand exactly what is happening at any point in the app's lifecycle.
- action creator - These are just normal JavaScript functions that return normal JavaScript Objects. Now, we can use this action creator function to dispatch an action to the store. ... Now, we just pass the tweet into our action creator function.
- reducer - A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. ... Redux relies heavily on reducer functions that take the previous state and an action in order to execute the next state.
- dispatch - dispatch is a function of the Redux store. You call store. dispatch to dispatch an action. This is the only way to trigger a state change. With React Redux, your components never access the store directly - connect does it for you.
