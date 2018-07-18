# Chapter 9 - Animations

### So how do we make animations in React Native?

We use mostly a declarative library called [Animated API](https://facebook.github.io/react-native/docs/animations#animated-api).

The steps to create a basic animation:

#### 1. We need to create a value to animate first and set it to an initial value:

```js
state = {
  animatedValue: new Animated.Value(0)
}
```
#### 2. Then we want to animate this value over time: 

```js
Animated.timing(
  this.state.animatedValue, // The value to drive
  {
    toValue: 100,     // Animate to final value of 1
    duration: 1000, // over 1 sec.
  }
).start(); // Start the animation
```

#### 3. And finally use it:

```js 
<Animated.View
  style={{
    width: 100,
    height: 100,
    backgroundColor: "steelblue",
    transform: [
      {
        translateX: this.state.animatedValue
      }
    ]
  }}
/>
```

### Which components can be animated? 

- Animated.Image
- Animated.ScrollView
- Animated.Text
- Animated.View

### Exercise
<insert animation 1 gif>

### Resources

- [Animatable Components](https://facebook.github.io/react-native/docs/animated#animatable-components)
