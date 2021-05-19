# Component Composition

## Refrences

- https://www.freecodecamp.org/news/these-are-the-concepts-you-should-know-in-react-js-after-you-learn-the-basics-ee1d2f4b8030/
- https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891
- https://reactjs.org/docs/composition-vs-inheritance.html
- https://testing-library.com/docs/react-testing-library/example-intro/
- https://www.npmjs.com/package/react-if
- https://testing-library.com/docs/dom-testing-library/api-async/

## Review, Research, and Discussion

1. Can a parent component access the state of a child component?

- In React we can access the child's state using Refs. we will assign a Refs for the child component in the parent component. then using Refs we can access the child's state.

2. What can be passed along in a prop variable?

- props enable you to pass variables from one to another component down the component tree. In the previous example, it was only a string variable. But props can be anything from integers over objects to arrays.

3. How can a child component “know” the state of another component?

- The most common method is to make a callback function that the child component will trigger and toss the state values upward.

## Vocabulary

- component props - Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
- component state - State is similar to props, but it is private and fully controlled by the component.
- application state - is simply the state at which an application resides with regards to where in a program is being executed and the memory that is stored for the application. The web is "stateless," meaning everytime you reload a page, no information remains from the previous version of the page.
