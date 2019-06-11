# Unit Testing with bff

[bff][1] is a node.js testing library similar to [jest][2] and [ava][3] but with a different set of features. It can be used for different kinds of tests but in this article we’ll start with some basic unit tests.

Let’s create a simple utility to format numbers:

```js
// index.js

class NumberFormatter {
	constructor (format) {
		this.format = format
	}

	format (number) {
		return number
	}
}

module.exports = NumberFormatter
```

Yea, it doesn't do anything, but let's prove it with a test:

```js
// tests.js

const { test } = require('@ianwalter')
const NumberFormatter = require('./index')

test('formatting a phone number', ({ expect }) => {
	const formatter = new NumberFormatter('(###) ###-####')
	const formatted = formatter.format(7805551234)
	expect(formatted).toBe('(780) 555-1234')
})
```

[1]:	https://github.com/ianwalter/bff
[2]:	https://jestjs.io
[3]:	https://github.com/avajs/ava