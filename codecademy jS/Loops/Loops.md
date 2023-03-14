A _loop_ is a programming tool that repeats a set of Instructions until a specified condition, called a _stopping condition_ is reached.

Iterating means repeating.

## The For Loop

* very handy for iterating over data structures, such as arrays.

```js
for (let counter = 0); counter < 4; counter++){
	console.log(counter)
	}
```

To loop in reverse. you would 
* set the iterator variable to the highest desired value in the initialization expression
* set the stopping condition when the iterator variable is less than the desired amount
* The iterator should decrease in intervals after each iteration 

## Nested Loops

* one use for nested loops is to compare the elements in two arrays
* for each round of the outer `for` loop, the inner `for` loop will run completely.

```js
const arr1 = [6, 19, 20];  
const arr2 = [19, 81, 2];  
for (let i = 0; i < arr1.length; i++) {  
  for (let j = 0; j < arr2.length; j++) {  
    if (arr1[i] === arr2[j]) {  
      console.log('Both arrays have the number: ' + arr2[j]);  
    }  
  }  
}
// first 6 will have 19, 81, 2 checked against it, then 19...
// Output: Both arrays have the number: 19

```


## While Loops

* the iterating variable is declared before the loop, but it will be accessible because it's in the global scope.
* next the `while` keyword is followed by the stopping / test condition.
* while loops are useful when you don't know how many times the loop should run (think of eating and not knowing exactly how many bites until feeling full)
```js
const cards = ['diamond', 'spade', 'heart', 'club'];

let currentCard;

while (currentCard !== 'spade'){

	currentCard = cards[Math.floor(Math.random() * 4)];

	console.log(currentCard)

}
```

## Do...While 

* runs at least once
* keep doing it until a specific condition is no longer met

```js
let countString = ''
let i = 0 
do {
	countString = countString + i;
	i++;
} while (i < 5)
```

## The `break` keyword


