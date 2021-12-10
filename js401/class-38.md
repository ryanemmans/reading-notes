# CLASS 38 NOTES - Redux - Asynchronous Actions

***1. How granular should your reducers be?***

- You should find a reasonable balance for granularity, based on how often fields are accessed and updated, and how much actual benefit selectors are providing in your application.

***2. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched***

- This may be either a pro or a con. It is a pro if your intention is to have a single action dispatching to more than one reducer to affect multiple pieces of state. It is a con if we did not initially intend to have certain state be changed.  

***3. Name a strategy for preventing the above***

- More specific and unique naming could prevent this.

***4. Document the following Vocabulary Terms:***

- **Store** - holds the whole state tree of your application. The only way to change the state inside it is to dispatch an action on it. A store is not a class. It's just an object with a few methods on it.
- **Combined reducers** - an example of a higher-order reducer, which takes an object full of slice reducer functions, and returns a new reducer function. A utility function to simplify the most common use case when writing Redux reducers.

- - -

## Preview:

- [Async Actions](https://redux.js.org/tutorials/fundamentals/part-6-async-logic)
- [Thunk Middlewear](https://github.com/reduxjs/redux-thunk)
- [Redux Thunk](https://www.digitalocean.com/community/tutorials/redux-redux-thunk)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Redux store
- Combined Reducers
- API integration

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Thunk
- Redux Middleware
- Async Redux actions

***3. What are you most excited about trying to implement or see how it works?***

- Material UI
- Gatsby
- Next.js

- - -

Sources:

- [Redux Style Guide](https://redux.js.org/style-guide/style-guide)
- [Redux Store](https://redux.js.org/api/store)
- [combineReducers](https://redux.js.org/usage/structuring-reducers/using-combinereducers)

[back](../README.md)
