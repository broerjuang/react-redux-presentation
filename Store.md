## Redux Store

In redux, we'll have three method when initiating store using createStore from redux.

```getState(), dispatch(), and subscribe()```


```javascript
const createStore = (reducer) => {
    let state;
    let listeners = [];

    const getState = () => state;

    const dispatch = action => {
        state = reducer(state, action);
        listeners.forEach(listener => listener())
    }

    const subscribe = (listener) => {
        listeners.push(listener);
        return () => {
            listeners = listeners.filter(l => l !== listener)
        }
    }

    dispatch({})
    return { getState, dispatch, subscribe}
}
```
