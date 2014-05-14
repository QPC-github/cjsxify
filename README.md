cjsxify
====

[Browserify](http://browserify.org/) transform for CJSX (CoffeeScript equivalent of JSX used in [React](http://facebook.github.io/react/) library by Facebook):

```coffeescript
# @cjsx React.DOM

React = require('react')

Hello = React.createClass
  render: ->
    <div>Hello, {@props.name}!</div>

React.renderComponent(<Hello name="World" />, document.getElementById('hello'))
```

Save the snippet above as `main.coffee` and then produce a bundle with the following
command:

    % browserify -t cjsxify main.coffee

`cjsxify` transform activates for files with either `.cjsx` extension or `# @cjsx React.DOM` pragma as a first line for any `.coffee` file.

### Installation
```bash
npm install -g coffee-react-transform
```

### Thanks
This package inspired by [coffeeify](https://github.com/jnordberg/coffeeify) and [reactify](https://github.com/andreypopp/reactify) use [coffee-react-transform](https://github.com/jsdf/coffee-react-transform) to handle `cjsx` transformation to `CoffeeScript`.
Thanks to the authors for their great work.
