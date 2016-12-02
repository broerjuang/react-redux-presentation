## Reducers

It has to be pure function

### Example
```javascript
let WelcomePage = (props) => {
  return (
    <div className="App">
    <div className="App-header">
      <img src={logo} className="App-logo" alt="logo" />
      <h2>Welcome to {props.react_text}, {props.children} Hacktiv8 !</h2>
    </div>
    <p className="App-intro">
      To get started, edit <code>src/App.js</code> and save to reload.
    </p>
  </div>
  )
}

class App extends Component {
  render() {
    return (
      <WelcomePage react_text="React" >Blandford Fox</WelcomePage>
    );
  }
}
```
Result
![](https://raw.githubusercontent.com/broerjuang/react-redux-presentation/master/example-react.png)