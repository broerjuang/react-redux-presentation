# Redux
> ...We're mixing two concepts that are very hard for the human mind to reason about: mutation and asynchronicity....managing the state of your data is left up to you. This is where Redux enters.

## Three Principles of Redux
- Single source of truth
  - [Juan Guardado on Redux Single Souce of Truth](https://medium.com/@juanguardado/redux-single-source-of-truth-e1fe1fb6ffec#.fhhk0x5xt)
- State is read-only
- Changes are made with pure functions

### 1. Single Source Of Truth
- People coming from different framework background have different interpretation about what it means.
- Does it more easy to maintain only a single source?

[State, Action, Reducer, ..](https://github.com/reactjs/redux/blob/master/docs/Glossary.md#action)

#### State
```javascript
type State = any
```
- It represents the entire state of a Redux application, which is often a deeply nested object.
- You should do your best to keep the state serializable.
- Don't put anything inside it that you can't easily turn into JSON.

### Action
```
type Action = Object
```
- An action is a plain object that represents an intention to change the state
- Actions are the only way to get data into the store
- Actions must have a type field that indicates the type of action being performed
- Types can be defined as constants and imported from another module
- It's better to use strings for type than Symbols because strings are serializable.

### Reducer
```
type Reducer<S, A> = (state: S, action: A) => S
```
- A reducer (also called a reducing function) is a function that accepts an accumulation and a value and returns a new accumulation
- [Javascript reduce ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)
- Reducers are the most important concept in Redux.

- Do not put API calls into reducers.
