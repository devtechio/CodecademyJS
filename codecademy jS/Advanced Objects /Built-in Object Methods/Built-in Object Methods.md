We can also take advantage of built-in methods for Objects: 
* .hasOwnProperty()
* .valueOf()

Object class methods : 
* Object.assign( )
* Object.entries( )
* Object.keys( )

```js
const robot = {
	model: 'SAL-1000',
	mobile: true,
	sentient: false,
	armor: 'Steel-plated',
	energyLevel: 75
};

// What is missing in the following method call?
const robotKeys = Object.keys(robot);
console.log(robotKeys);

// Declare robotEntries below this line:
const robotEntries = Object.entries(robot)
console.log(robotEntries);
  
// Declare newRobot below this line:
const newRobot = {}
Object.assign (newRobot, robot, {laserBlaster: true, voiceRecognition: true})  

console.log(newRobot// );

  
// Output:

// { model: 'SAL-1000',
  // mobile: true,
  // sentient: false,
  // armor: 'Steel-plated',
  // energyLevel: 75,
  // laserBlaster: true,
  // voiceRecognition: true }
```



