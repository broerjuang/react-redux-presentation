# Pure Function

## A pure function is a function which:
* Given the same input, will always return the same output.
* Produces no side effects.
* Relies on no external state.

## Example

### Pure Function
```javascript
let add = (a, b) => { return a + b }

console.log(add(5, 5))

```

### Impure Function
```javascript
let count = 5;

let add = (param) => { return param + count }

console.log(add(5))

```

### Pure Function
```javascript
let squareAll = (items) => {

  let len = items.length;
  for (var i = 0; i < len; i++) {
    items[i] = items[i] * items[i];
  }

  return items;
}

console.log(squareAll([0, 1, 2, 3, 4]))
```

### Impure Function
```javascript
let squareAllPure = (items) => {
  return items.map((item) => {
    return item = item**2
  })
}

console.log(squareAllPure([0, 1, 2, 3, 4]))
```