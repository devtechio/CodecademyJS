A block is the code found inside a set of curly braces { }

Blocks help us group one or more statements together and serve as an important structural marker for our code.

A block of code could be a function.
A block of code could be in an if statement

```js
const logSkyColor = () => {  
  let color = 'blue';  
  console.log(color); // blue  
}
// Notice that the function body is actually ab lock of code.

if (dusk) {  
  let color = 'pink';  
  console.log(color); // pink  
}
// Block of an if statement
```

# Global Scope

Scope is the context  in which our variables are declared.  We think about scope in relation to blocks because variables can exist either outside or within these blocks.

In _global_ scope variables are declared outside of blocks.
 * because global variables live on the **outside** of a block of code, they can be accessed by an code in the program, including the code within blocks.

```js
const color = 'blue';  
  
const returnSkyColor = () => {  
  return color; // blue  
};  
  
console.log(returnSkyColor()); // blue
```


# Block Scope

When a variable is defined inside a block, it is only accessible to the code within the curly braces { }.

Variable is block scoped when it's only accessible to the lines of code within that block.

```js
const logSkyColor = () => {  
  let color = 'blue';  
  console.log(color); // Prints "blue"  
};  
  
logSkyColor(); // Prints "blue"  
console.log(color); // throws a ReferenceError
```

# Scope Pollution

Having too many global variables can cause problems in a program.

**_Scope Pollution_** is when we have too many global variables that exist in the global namespace, or when we reuse variables across different scopes.
```js
let num = 50;  
  
const logNum = () => {  
  num = 100; // Take note of this line of code  
  console.log(num);  
};  
  
logNum(); // Prints 100  
console.log(num); // Prints 100
```

### Practice Good Scoping Habits

Scope variables as tight as possible.
