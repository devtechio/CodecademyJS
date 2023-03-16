# The `this` keyword

```js
const goat = {
	dietType: 'herbivore',
	makeSound() {
		console.log('baaa')
	}
}

goat.makeSound() // 'baaa'
```

If we wanted a new method, .diet() to print out the existing dietType:

```js
const goat = {  
  dietType: 'herbivore',  
  makeSound() {  
    console.log('baaa');  
  },  
  diet() {  
    console.log(dietType);  
  }  
};  
goat.diet();  
// Output will be "ReferenceError: dietType is not defined"
```
* That’s because inside the scope of the `.diet()` method, we don’t automatically have access to other properties of the `goat` object.
```js 
const goat = {  
  dietType: 'herbivore',  
  makeSound() {  
    console.log('baaa');  
  },  
  diet() {  
    console.log(this.dietType);  
  }  
};  
  
goat.diet();  
// Output: herbivore
```
* The `this` keyword references the _calling object_ which provides access to the calling object’s properties
* In calling object is `goat` and then the `dietType` property of goat is accessed by using dot notation.
```js
	const robot = {
		model : '1E78V2',
		energyLevel: 100,
		provideInfo () {
		return `I am ${this.model} and my current energy level is ${this.energyLevel}.`
		}
};

console.log(robot.provideInfo())
// I am 1E78V2 and my current energy level is 100.
```

# Arrow Functions and this

We saw earlier that if we use `this` keyword in a method then the value of `this` is the calling object.  It becomes more complicated when we start using arrow functions for methods: 

```js
const goat = {  
  dietType: 'herbivore',  
  makeSound() {  
    console.log('baaa');  
  },  
  diet: () => {  
    console.log(this.dietType);  
  }  
};  
  
goat.diet(); // Prints undefined
```

* Arrow functions inherently _bind_ an already defined `this` value to the function itself that is NOT the calling object. In this case, the value of `this` would be the _global object_ / an object that exists int he _global scope_, which doesn't have a `dietType` property, and that's why: `undefined` 


