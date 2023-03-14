ES6 introduced a shorter way to write functions by using the _fat arrow_ ( ) => notation; the arrow function removes the need to type out the word `function` .

![[Screenshot 2023-03-12 at 10.28.36 AM.png]]

## Concise Body Arrow Functions 

There are several ways to refactor arrow function syntax: 

* If the function takes a single parameter, you don't need parenthesis around it. If it is zero or more, you do.
* A function body that has a single-line block doesn't need curly braces. Without them, whatever the line evaluates to is automatically returned; thus the return keyword can be removed: <mark class="hltr-green">implicit return</mark>.
![[parameters_arrow_functions.png]]
![[consise_arrow_functions.png]]

```js
const squareNum = (num) => {  
  return num * num;  
};
```

= 

```js
const squareNum = num => num * num;
```

