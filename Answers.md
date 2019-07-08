1.  Name 3 JavaScript Array/Object Methods that do not produce side-effects? Which method do we use to create a new object while extending the properties of another object?

Three Javascript Array/Object methods that do not produce side-effects are `.map()`, `.filter()`,`.concat()`. We can use `Object.assign()` if we want to creates a brand new object and adds new key/value pairs/extend the properties of another object.

2.  Describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

`actions` in Redux are the packets of information, usually an object, that contain an action type and a "payload" that contains some data for that action type.
The`reducers` handle those actions and replace the store accordingly; reducers are pure functions.
The `store` is a single JavaScript Object that contains our state for our application;
the `store` is the single source of truth in the application in that when we make changes to our state object, we do not write over or mutate the original state object directly, but we copy the state object, modify the copy, and replace the original state with the new copy.

3.  What is the difference between Application state and Component state? When would be a good time to use one over the other?

Application state is global and component state is local. Redux uses the store to hold application state. Meaning any component in the app can access it as long as they connect into it. The component state can only be updated within that specific component and passed down to its children through props.

4.  What is middleware?

Middleware is software glue that enables us to connect bits of software together easily; middleware allows us to intercept or intervene in processes and allow processes to continue or not

5.  Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?

Redux-thunk is a middleware that allows you to write actions creators that return a function instead of an action. It can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. That function receives the store's dispatch method, which is then used to dispatch regular synchronous actions inside the body of the function once the asynchronous operations have completed.

6.  Which `react-redux` method links up our `components` with our `redux store`?

`connect` links up our components with the `redux store`
