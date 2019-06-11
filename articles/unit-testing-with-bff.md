# Unit Testing with bff

[bff][1] is a node.js testing library similar to [jest][2] and [ava][3] but with a different set of features. It can be used for different kinds of tests but in this article we’ll start with some basic unit tests.

Let’s create a simple utility to

```js
class NumberFormatter {
	constructor (format) {
		this.format = format
	}

	format (number) {
		
	}
}
```

[1]:	https://github.com/ianwalter/bff
[2]:	https://jestjs.io
[3]:	https://github.com/avajs/ava