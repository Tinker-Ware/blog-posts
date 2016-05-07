I have been using [React.js](https://facebook.github.io/react/index.html), a JavaScrip library for creating user interfaces, for about 4 months now.  You might want to read the official [getting-started](https://facebook.github.io/react/docs/getting-started.html) or [Tutorial](https://facebook.github.io/react/docs/tutorial.html) pages.

**React has the following advantages:**

* Good if you what to build large applications with data that changes over time.
* **Virtual DOM**. React abstracts away the DOM, giving a simple programming model and better performance.
* Implements one-way reactive data flow.
* Is based in components.
* Is the V in MVC.
* You can always change how the component will render looking at one source file.
* Building Javascript and HTML into JSX makes components easily understandable.
* React.js is declarative, which means that React conceptually hits the “refresh” button any time data changes.
You can use React.js seamlessly with Node.js or AngularJS.

This is an component example:

`var HelloMessage = React.createClass({
    render: function() {
      return <div>Hello {this.props.name}</div>;
    }
  });
  ReactDOM.render(<HelloMessage name="John" />, mountNode);`


**Recommendations:**

* Use [React.js](https://facebook.github.io/react/index.html) only if your application have very much dynamic page updating.
* Break the UI into a component hierarchy.
Use [Redux](http://redux.js.org/) instead of [Flux](https://facebook.github.io/flux/).
* Write test of each of your components
* Use JSX, ES6, Babel, Webpack, and NPM.
* Use the React and Redux dev tools.
* Write small components.

If you know the absolute basics use [React Slingshot](https://github.com/coryhouse/react-slingshot) starter kit for rapid application development using React.

**That's it!**

If you enjoyed this post, you might like to follow me on [Twitter](https://twitter.com/ileonelperea), and follow me on [Github](https://github.com/iLeonelPerea).

Thanks for reading!