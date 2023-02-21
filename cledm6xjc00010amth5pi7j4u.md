# React redux rules

## Redux State Management:

1. Use actions to describe events that occur in your application.
    
2. Create action types as constants to avoid spelling errors and collisions.
    
3. Use action creators to encapsulate the logic of creating actions.
    
4. Use reducers to describe how the state is updated when an action is dispatched.
    
5. Keep reducers pure by avoiding side effects.
    
6. Use the spread operator to create new state objects when updating state.
    
7. Always return a new state object from a reducer.
    
8. Use the combineReducers utility function to combine multiple reducers into one.
    
9. Keep your store simple by limiting the number of reducers.
    
10. Use selectors to compute derived data from your application state.
    
11. Use middleware to handle side effects and async actions.
    
12. Use thunks to dispatch async actions.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676945497154/79858e0c-c5ef-4481-810a-b8e63dc66588.gif align="center")

##   
Redux Toolkit Best Practices:

1. Use the `createSlice` function to create Redux slices, which reduces boilerplate and simplifies code.
    
2. Use the `createAsyncThunk` function for handling async actions.
    
3. Use the `createEntityAdapter` function to manage entities in the state.
    
4. Use the `configureStore` function to set up your Redux store with pre-configured middleware, reducers, and other options.
    
5. Use the `immer` library to write immutable updates to your state.
    

## Redux Style Guide:

1. Name actions with present tense verbs that describe what happened, such as "incrementCounter" or "setUser".
    
2. Use uppercase letters and underscores to separate words in action types.
    
3. Use lowercase letters and camel case to name reducers, such as "counterReducer".
    
4. Avoid nesting your state too deeply, as this can make it harder to work with and debug.
    
5. Use constants or enums for action types, to avoid typos and make your code more readable.
    
6. Use the Redux Toolkit `createAsyncThunk` function for handling asynchronous logic.
    
7. Use the `configureStore` function to set up your Redux store, with middleware and other options pre-configured.
    

These are just some of the best practices and rules to follow when working with Redux and Redux Toolkit. By following these guidelines, you can ensure that your code is maintainable, scalable, and follows best practices for state management.