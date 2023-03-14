* In addition to allowing us to reuse our code, functions help to make clear, readable programs
* _Higher-order functions_ are functions that accept other functions as arguments and/or return functions as output. This enables us to build abstractions on other abstractions

```js
const testFunction = () =>{
	console.log('Hello, World!')
}
const test = testFunction

test()
```

* in this example test is a reference to the original testFunction reference, they would point to the same place in memory.

* functions are <mark class="hltr-cyan">first-class objects</mark> meaning functions can have properties and methods.
* functions are special because we can invoke them, but we can still treat them like any other type of data.

A _higher-order function_ is a function that either accepts functions as parameters, returns a function or both.

Since functions behave like any other data-type in JS, they can also be passed as parameters in functions.

* functions that get passed as a parameter are called <mark class="hltr-cyan">callback functions</mark>
* with callback functions, we pass in the function without the parenthesis

