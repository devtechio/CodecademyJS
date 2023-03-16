There are cases in which we don't want other code accessing and updating an object's properties. 

<mark class="hltr-cyan">`Privacy` therefore is the idea that only certain properties should be mutable / change in value.</mark>

* certain languages have privacy built-in for objects, but JavaScript does not have this feature.
   * Javascript developers place an underscore _ before the name of a property to mean the property should not be altered.
   ```js 
	const bankAccount = {
		_amount: 1000
	}
```

## Getters 

* Getters are methods that get and return the internal properties of an object, but they can do more.
```js
const person = {  
  _firstName: 'John',  
  _lastName: 'Doe',  
  get fullName() {  
    if (this._firstName && this._lastName){  
      return `${this._firstName} ${this._lastName}`;  
    } else {  
      return 'Missing a first name or a last name.';  
    }  
  }  
}  
  
// To call the getter method:  
person.fullName; // 'John Doe'
```

* last line we call `fullName` on `person` ; in general getter methods do not need to be called with a set of ( ), so it looks as though we're accessing a property.

#### Advantage of using Getter methods

-   Getters can perform an action on the data when getting a property.
-   Getters can return different values using conditionals.
-   In a getter, we can access the properties of the calling object using `this`.
-   The functionality of our code is easier for other developers to understand.

```js
const robot = {
	_model: '1E78V2',
	_energyLevel: 100,
	get energyLevel (){
		if(typeof(this._energyLevel) === 'number') {
			return `My current energy level is ${this._energyLevel}`
		} else {
			return 'System malfunction: cannot retrieve energy level'
		}
	}
};
  
console.log(robot.energyLevel)// My current energy level is 100
```

## Setters 

Setter methods reassign values of existing properties within an object 

```js
const person = {  
  _age: 37,  
  set age(newAge){  
    if (typeof newAge === 'number'){  
      this._age = newAge;  
    } else {  
      console.log('You must assign a number to age');  
    }  
  }  
};


const robot = {
		_model: '1E78V2',
		_energyLevel: 100,
		_numOfSensors: 15,
		get numOfSensors(){
			if(typeof this._numOfSensors === 'number'){
				return this._numOfSensors;
			} else {
				return 'Sensors are currently down.'
		}
	},

	set numOfSensors(num) {
		if (typeof num === 'number' && num >= 0){
			this._numOfSensors = num
		} else {
		console.log('Pass in a number that is greater than or equal to 0')
		}
	}
};
robot.numOfSensors = 100
console.log(robot.numOfSensors) // 100
```



