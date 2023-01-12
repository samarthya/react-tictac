# Application Tic-Tac-Toe

The application being built is a simple game of `0` and `X` that allows 2 users to interactively play under specific rules of winning & draw.

This tutorial builds that appliction using React as the enabler to build the complete application.

## Component Game

```js
class Game extends React.Component 
```

## Component Board

Board is the representation of the 9 squares arranged in `3x3` format.

```js
class Board extends React.Component
```

## Component Square

Squre is an individual box that recieves input from the user and stores it till the game ends.

```js
class Square extends React.Component 
```

### Defining state for Square

You should call `super(props)` before any other statement. Otherwise, `this.props` will be undefined in the constructor, which can lead to bugs.

#### Constructor defined

```js
constructor(props) {
        super(props);
        // Define the state
        this.state = {
            value: null,
        };
    }
```

##### Remember 

- When you call `setState` in a component, React automatically updates the child components inside of it too.

```js
render() {
        return (
            <button className="square"
                onClick={() => this.setState({ value: 'X' })}>
                {this.state.value}
            </ button>
        );
    }
```

## Helpful Links

- [Arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)