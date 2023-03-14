![Diagram outlining an array literal that has 3 separate elements, a comma separates each element (a string, a number, and a boolean) and the elements are wrapped with square brackets](https://content.codecademy.com/courses/learn-javascript-arrays/array%20literal.svg)


* Each item in an array is called an element
* We can save arrays to variables
* You can put any data type in an array
* Array can be thought of as making lists


## Accessing Elements

Each element in an array has a numbered position : _index

Arrays in JS are _Zero Indexed_
* We use bracket notation with the index after the name of the array to access an element within the array:
```js
let cities = ['LA', 'NYC', 'SF']
cities[0] // 'LA'

```  

  
* you can also use bracket notation to access characters in a string 
```js
const hello = 'Hello World';  
console.log(hello[6]);  
// Output: W
```
* if you try to access an element beyond the last item in an array, `unefined` will be logged.

*   Index 0 has the first element.
-   Index 1 has the second element.
-   Index 2 has the third element.
-   Index n-1 has the nth element.

## Updating Elements

Once you have access to an element you can update its value

```js
let seasons = ['Winter','Spring','Summer','Fall']

seasons[3] = 'Autumn'
console.log(seasons)

//['Winter','Spring','Summer','Autumn']
```

### Arrays with let and const

##### Variables declared with `const` cannot be reassigned, but elements in an array declared with `const` remain mutable  (able to change)

### The .length property

.length returns the number of items in an array

```js
const newYearsResolutions = ['Keep a journal', 'Take a falconry class'];  
  
console.log(newYearsResolutions.length);  
// Output: 2
```







# Array Methods

## The .push( ) method

* `.push( )` allows us to add items to the end of an array, 
* mutates the inital array.

## The .pop( ) method

* `.push( )` removes the last item of an array.
* mutates the initial array

```js
const removed = arrayExample.pop()
```


## The .shift( ) method

* .shift( ) removes the first item of an array.
* mutates the initial array



## The .unshift( ) method

* .unshift()
* Adds one or more elements to beginning of array and returns new length.



## The .slice( ) method

* returns a shallow copy of all or part of an array
* does not mutate initial array

```js
array.slice(start, end)
 
```

* start: the start index of the slice to be returned (optional)
*  end: the end index of the slice index to be returned (optional) 
* The returned array contains the element specified by the first argument and all subsequent elements up to, but not including, the element specified by the second argument.
```js 
array.slice(start)
```
* If one argument is specified, the returned array contains all the elements from the start to the end of the array
```js 
array.slice() 
```
* if no argument is specified, the returned array will be the whole array

```js
const weekdays = ['Monday','Tuesday','Wednesday','Thursday','Friday','Saturday','Sunday']

const outOfOffice = weekdays.slice(1,4) 
// creates of a subarray of :
['Tuesday', 'WeÎdnesday', 'Thursday']
```

## Nested Arrays

```js
const food = [
['Apple', 'Orange', 'Banana'],
['Strawberry', 'Blueberry', 'Raspberry'],
['Potato','Carrot','Broccoli'][]()
]


food[1][2] //'Raspberry'
food[0][1] //'Orange'

const nestedArray = [

[
	[1, 2],
	[3, 4],
	[5, 6],
],

[
	['A', 'B', 'C'],
	['D', 'E', 'F'],
],

];

console.log(nestedArray[1][0][2]) //'C'
console.log(nestedArray[0][1][1]) // 4
```


