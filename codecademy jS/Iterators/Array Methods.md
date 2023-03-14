## .forEach( ) method

* will execute the same for each element in an array

![Diagram outlining the parts of an array iterator including the array identifier, the section that is the iterator, and the callback function](https://content.codecademy.com/courses/learn-javascript-iterators/iterator%20anatomy.svg)

-   The return value for `.forEach()` will always be `undefined`.

```js
const fruits = ['mango', 'papaya', 'pineapple', 'apple'];

// Iterate over fruits below

fruits.forEach(fruit =>
	console.log('I want to eat a ' + fruit))

// I want to eat a mango
// I want to eat a papaya
// I want to eat a pineapple
// I want to eat a apple
```

## .map( ) method

* When .map() is called on an array, it takes an argument of a callback function and returns a new array
* .map() works similar to .forEach() but the main difference is that .map() returns a new array.

```js
const numbers = [1, 2, 3, 4, 5];  
  
const bigNumbers = numbers.map(number => {  
  return number * 10;  
});

console.log(bigNumbers); // Output: [10, 20, 30, 40, 50]
```

## .filter ( ) method

* Like `.map()`, `.filter()` returns a new array. However, `.filter()` returns an array of elements after filtering out certain elements from the original array.

```js
const words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door'];  
  
const shortWords = words.filter(word => {  
  return word.length < 6;  

console.log(shortWords); // Output: ['chair', 'music', 'brick', 'pen', 'door']
```

## .findIndex ( ) method

* Calling .findIndex() on an array will return the index of the first element that evaluates to `true` in the callback function.

```js 
const jumbledNums = [123, 25, 78, 5, 9];  
  
const lessThanTen = jumbledNums.findIndex(num => {  
  return num < 10;  
});
```

## .reduce ( ) method

* the .reduce() method returns a single value after iterating through the elements of an array, thereby _reducing_ the array

```js
const numbers = [1, 2, 4, 10];  
  
const summedNums = numbers.reduce((accumulator, currentValue) => {  
  return accumulator + currentValue  
})  
  
console.log(summedNums) // Output: 17
```

![[Screenshot 2023-03-14 at 12.57.13 PM.png]]

* The `.reduce()` method can also take an optional second parameter to set an initial value for `accumulator` (remember, the first argument is the callback function!). 



