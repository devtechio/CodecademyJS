Before:
```js 
	const monsterFactory = (name, age) => {
		return {
			name: name,
			age : age
		}
	}
```
After: 
```js
	const monsterFactory = (name, age) => {
		return {
			name,
			age
		}
	};
```

# Destructured Assignment 

```js 
	const vampire = { 
		name: 'Dracula',
		residence: 'Transylvania',
		preferences: {
			day: 'stay inside',
			night: 'satisfy appetite'
		}
	}
```
Before: 
```js
const residence = vampire.residence;
console.log(residence) // 'Transylvania'
```
After: 
```js
	const { residence } = vampire;
	console.log(residence) // 'Transylvania'
```

```js
	const robot = {
		model: '1E78V2',
		energyLevel: 100,
		functionality: {
			beep() {
				console.log('Beep Boop');
				},
			fireLaser() {
				console.log('Pew Pew');
				},
		}
	};

const {functionality} = robot

functionality.beep() // 'Beep Boop'
```

