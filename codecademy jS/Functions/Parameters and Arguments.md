## Parameters and Arguments

When declaring a function, we can specify its parameters; which allow functions to accept input(s) and perform a task with the input(s).

![[function_parameters.png]]

![[function_arguments.png]]

When calling a function that has parameters, such as calculateArea, the values that are passed to the function when its called are called *arguments*.

#### Default Parameters

One of the features added in **_ES6_**  is the ability to use _default parameters_ which allow parameters to have predetermined values in case no arguments are passed into the function, or if the argument is _undefined_ when it's called.

```js
function calculateArea(width = 4, height) {
	console.log(width * height);
}
```

#parameters
#arguments
#default_parameters
