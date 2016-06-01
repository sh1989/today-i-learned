# Functional Components

As of React 14, it's possible to utilise anonymous functions to create React components, rather than using `React.createClass`. These are useful when the React components that you wish to create are stateless - i.e. they render purely based on their supplied props.

So instead of:

```
const MyComponent = React.createClass({
  render: function() {
    return <p>Hello, <span>{this.props.name}</span></p>;
  }
});
```

We can do:

```
const MyComponent = (props) => {
  return <p>Hello, <span>{props.name}</span></p>;
};
```

There's a few things to note here:

* You can still define `propTypes` and `defaultProps`
* You don't have access to other lifecycle methods - for those you'll need a full React class.
* No component instance is created, so `refs` will evaluate to `null`.
