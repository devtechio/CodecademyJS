* we can use objects to model real-world things, or we can use objects to build the data structures that make the web possible 

* Primitive data types in JS: 
* strings, numbers, objects, boolean, undefined, null and symbol.
  
  * We fill an object with unordered data. This data is organized into _key-value pairs_. A key is like a variable name that points to a location in memory that holds a value.

```js
// An object literal with two key-value pairs  
let spaceship = {  
  'Fuel Type': 'diesel',  
  color: 'silver'  
};
```

## Accessing properties

* There are two ways of accessing an object property.

#### Dot Notation

```js
let spaceship = {  
  homePlanet: 'Earth',  
  color: 'silver'  
};  
spaceship.homePlanet; // Returns 'Earth',  
spaceship.color; // Returns 'silver',
```

* If we try to access a property that does not exist on that object, `undefined` will be returned.

#### Bracket Notation

* We **must** use bracket notation when accessing keys that have <mark class="hltr-cyan">numbers, spaces, or special characters</mark> in them.
* you can also use a variable inside the brackets to select the keys of an object

## Property assignment 

* Objects are mutable / updatable 
* Can use both dot or bracket notation + an assignment operator `=` to add new key-value pairs.

One of two things can happen with property assignment:

-   If the property already exists on the object, whatever value it held before will be replaced with the newly assigned value.
-   If there was no property with that name, a new property will be added to the object

You can delete a property from an object with the `delete` operator.

```js
spaceship.color = 'glorious gold'
spaceship.numEngines = 5;
delete spaceship['Secret Mission']
```

# Methods

* When the data stored on an object is a function, we call that a method.
   * a property is what an object has
   * a method is what an object does.
   * object methods are invoked by appending the object's name with a dot operator followed by a method name + parenthesis

```js
console.log() // console = global object .log() is a method on that object
Math.floor()  // Math = global JS object .floor() = method
```

```js
const neighborly = {
	sayHi () {
		console.log('Hi, how are you?')
	}
};
```



# Nested Objects

* In application code, objects are often nested— an object might have another object as a property which in turn could have a property that’s an array of even more objects


# Pass by reference 

* primitives pass by value
* objects /array obj pass by reference (they point to the same thing in memory)
* objects are passed by reference which means when we pass a variable assigned to an object into a function as an argument, the computer interprets the parameter name as pointing to the space in memory holding that object; as a result, functions which change object properties actually mutate the object permanently even when the object is assigned to a `const` variable.

# Looping through objects

* key-value pairs are not ordered like the numerical indexing of arrays
* so we use for...in which will execute a given block of code for each property in an object
```js
let spaceship = {

		crew: {

	     captain: {
				name: 'Lily',
				degree: 'Computer Engineering',
				cheerTeam() { console.log('You got this!') }
				},
		'chief officer': {
				name: 'Dan',
				degree: 'Aerospace Engineering',
				agree() { console.log('I agree, captain!') }
				},
		medic: {
				name: 'Clementine',
				degree: 'Physics',
				announce() { console.log(`Jets on!`) } 
				},
		translator: {
				name: 'Shauna',
				degree: 'Conservation Science',
				powerFuel() { console.log('The tank is full!') }

				}
			}

	};

	for (let crewRole in spaceship.crew){

console.log(`${spaceship.crew[crewRole].name}: ${spaceship.crew[crewRole].degree}`)

}

// Lily: Computer Engineering
// Dan: Aerospace Engineering
// Clementine: Physics
// Shauna: Conservation Science
```


