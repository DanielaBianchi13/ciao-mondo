# ciao-mondo
just another respository
Sono appena arrivata in questo mondo stupendo, se vi chiedessi aiuto rispondete please! :)
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Basic Click Counter Example with JSX</title>
    <link rel="stylesheet" href="../shared/css/base.css" />
  </head>
  <body>
    <h1>Basic Click Counter Example with JSX</h1>
    <div id="container">
      <p>
        To install React, follow the instructions on
        <a href="https://github.com/facebook/react/">GitHub</a>.
      </p>
      <p>
        If you can see this, React is <strong>not</strong> working right.
        If you checked out the source from GitHub make sure to run <code>grunt</code>.
      </p>
    </div>
    <h4>Example Details</h4>
    <p>This is written with JSX and transformed in the browser.</p>
    <p>This example uses events and state to track clicks and update the rendered output.</p>
    <p>
      Learn more about React at
      <a href="https://facebook.github.io/react" target="_blank">facebook.github.io/react</a>.
    </p>
    <script src="../../build/react.js"></script>
    <script src="../../build/react-dom.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.24/browser.min.js"></script>
    <script type="text/babel">
      var Counter = React.createClass({
        getInitialState: function () {
          return { count: 0 };
        },
        handleClick: function () {
          this.setState({
            count: this.state.count + 1,
          });
        },
        render: function () {
          return (
            <button onClick={this.handleClick}>
              Click me! Number of clicks: {this.state.count}
            </button>
          );
        }
      });
      ReactDOM.render(
        <Counter />,
        document.getElementById('container')
      );
    </script>
  </body>
</html>
