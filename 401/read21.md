# Props and State

## refrences

- https://css-tricks.com/understanding-react-setstate/
- https://reactjs.org/docs/handling-events.html
- https://reactjs.org/docs/forms.html
- https://reactjs.org/docs/state-and-lifecycle.html
- https://reactjs.org/docs/components-and-props.html
- https://testing-library.com/docs/dom-testing-library/react-testing-library
- https://thomaslombart.com/beginner-guide-testing-react-apps/
- https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#roles

## Review, Research, and Discussion

1. Does a deployed React application require a server?

- You don't necessarily need a static server in order to run a Create React App project in production. It also works well when integrated into an existing server side app

2. Why do we prefer to test a React application at the behavior rather than the unit level?

- To get the most accurate represenation of the app running in the browser

3. What does npm run build do?

- npm run build creates a build directory with a production build of your app. Set up your favorite HTTP server so that a visitor to your site is served index. html , and requests to static paths like /static/js/main.

4. Describe the actual composition / architecture of a React application

- your "app" is the outline of the all the "componets" and holds those in how ever you want or need.... its like

## Vocabulary

- BDD - Behavior Driven Development is a software development approach that allows the tester/business analyst to create test cases in simple text language (English). The simple language used in the scenarios helps even non-technical team members to understand what is going on in the software project.
- Acceptance Tests - testing technique performed to determine whether or not the software system has met the requirement specifications. The main purpose of this test is to evaluate the system's compliance with the business requirements and verify if it is has met the required criteria for delivery to end users.
- mounting - is the phase in which our React component mounts on the DOM (i.e., is created and inserted into the DOM). This method is called just before a component mounts on the DOM or the render method is called. After this method, the component gets mounted.
- build - npm run build creates a build directory with a production build of your app.
