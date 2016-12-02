```javascript
import React, { Component } from 'react';
import { createStore } from 'redux';

const reducer = (state, action) => {
  if(action.type === 'INCREMENT'){
    return state + action.payload
  } 
  if(action.type === 'DECREMENT'){
    return state - action.payload
  }
  if(action.type === 'MULTIPLE') {
    return state * action.payload
  } 
  return state;
}

const store = createStore(reducer, 0)

store.subscribe(() => {
  console.log('hey dude the store change', store.getState())
})

store.dispatch({type: "INCREMENT", payload: 1})
store.dispatch({type: "INCREMENT", payload: 1})
// store.dispatch({type: "DECREMENT", payload: 1})
store.dispatch({type: "INCREMENT", payload: 1})
store.dispatch({type: "DECREMENT", payload: 1})
store.dispatch({type: "MULTIPLE", payload: 3})

class App extends Component {
  render() {
    return (
      <h1> Redux Training</h1>
    );
  }
}

export default App;
```
