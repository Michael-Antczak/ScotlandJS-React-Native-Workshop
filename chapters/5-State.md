# Chapter 5 - State and Lifecycle Methods

## Lifecycle methods

[React Lifecycle methods diagram](http://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)

[Walkthrough a code sample for using State](https://codepen.io/gaearon/pen/amqdNA?editors=0010)

## Common Patterns

These are some common patterns where `state` used in a typical RN application.

### Fetching Data through AJAX

```js
const ApiKey = 'AIzaSyD5tpHMFE1lKy2XQym1KB30uSjW12qVWHY';
const searchQuery = 'Codebase Edinburgh';
const url = `https://maps.googleapis.com/maps/api/place/findplacefromtext/json?input=${searchQuery}&inputtype=textquery&fields=photos,formatted_address,name,rating,opening_hours,geometry&key=${ApiKey}`

componentDidMount() {
    fetch(url).then(response => response.json())
        .then((data) => {
            this.setState({ placeInfo: data })
        })
}
```

or using `async/await`

```js
async componentDidMount() {
    const response = await fetch(url)
    const data = await response.json()
    this.setState({placeInfo: data})
}
```

### Keeping track of form values

```js
  constructor(props) {
    super(props);
    this.state = {searchQuery: ''};
  }

  render() {
      return (<TextInput
          style={{height: 40}}
          placeholder="Type here to translate!"
          onChangeText={(searchQuery) => this.setState({searchQuery})}
        />)
  }
```

> **RN Wisdom**: Controversial, but ... use local state (if that's all you need - in a form for example) even if you're using a state management solution like Redux.

### Resources
- [React component](https://reactjs.org/docs/react-component.html)
- [State and lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
- [Networking](https://facebook.github.io/react-native/docs/network)
