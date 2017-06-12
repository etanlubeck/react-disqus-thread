# react-disqus-comments

## This is a fork
Forked from the popular package by mzabriskie, but with a few fixes.
Added Single Sign-On support.

Also adds the optional `targetWindow` property to allow disqus to embed
in windows other than the default.

## Installing

```bash
$ npm install react-disqus-comments-sso
```

## Example

```js
var React = require('react');
var ReactDisqusComments = require('react-disqus-comments-sso');

var App = createClass({

	handleNewComment: function(comment) {
		console.log(comment.text);
	}

	render: function () {
		return (
			<ReactDisqusComments
				shortname="example"
				identifier="something-unique-12345"
				title="Example Thread"
				url="http://www.example.com/example-thread"
				category_id="123456"
				onNewComment={this.handleNewComment}
				api_key="PUBLIC KEY"
				remote_auth_s3=""
				targetWindow={window} // Optional
				/>
		);
	}
});

React.render(<App/>, document.getElementById('container'));
```

## License

MIT
