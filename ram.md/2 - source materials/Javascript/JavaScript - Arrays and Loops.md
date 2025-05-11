09-04-2025 11:59:13

Status : #child 

Tags : [[Introduction to JavaScript]] [[Arrays]] 

## [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

- Not type based, but can be type specific using type [Javascript typed arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Typed_arrays)
- Initialized with `[]` brackets
- Array is a object of Javascript, so they have properties and methods such as,
	1. length property
	2. push method 
-  Arrays are references with de-structuring feature.

```javascript
const myArray = [1,'hellow', true, null, undefined, [1,2,3], {name : 'socks'}]; // this is an array with different data types
console.log(myArray); 

console.log(myArray[0]); // this will give the first element of the array
console.log(myArray[myArray.length - 1]); // this will give the last element of the array

myArray[0] = 10; // this will change the first element of the array
console.log(myArray); // this will give the updated array

console.log(typeof myArray); // this will give the type of the array
console.log(Array.isArray(myArray)); // this will give true if the array is an array

myArray.push(100); // this will add the element to the end of the array
console.log(myArray); // this will give the updated array

//array destructuring
const [one, two, three] = myArray; // this will destructure the array into three variables
console.log(one); // this will give the first element of the array
console.log(two); // this will give the second element of the array     
```

## [Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)

Looping through an array

```javascript
[
	'hi',
	'hellow',
	'world'
].forEach(function(value, index){    // value of eachItem is in value
	if (value === 'hellow'){
	return;     // returns to the next loop. similar to continue 
	}
	console.log(value);
	console.log(index);    // index of eachItem is in index
}
);
```

> there is no convenient way to break from forEach loop so use noraml for loop if you want to break out of the loop.
## Advanced Functions

- functions can be saved in a variable, and can be called by just using the variable, since we can call a function with a variable we don't need a function name these kinds of functions are called as *anonymous functions*.
- In javascript if we use the function keyword and create a function it is available to be called in any order, this phenomenon is called *hoisting*

setTimeout - takes two parameters such as function and milli-seconds to wait

```javascript
setTimeout(    // will print timeout after 3 seconds
	function(){
		console.log('timeout');
	},
	3000     // sets a timer of 3 seconds
)

console.log('next line');
```

> setTimeout is a Asynchronous code, meaning it doesn't stop the execution of the program but sets a timer to call the given function, that's why we see next line before timeout. 

setInterval - takes two parameters such as a function and milli-seconds to repeat the function and wait for the time interval

```javascript
setInterval(    // this will run the function every 1 second
		function() {
				console.log('interval 1');
		}, 1000
);
```

### Arrow functions

```javascript
// regular function
function add(a, b) {
	console.log(a + b);    
	return a + b;  
}
add(34, 35);
```

```javascript
// arrow function
const add = (a, b) => {    // for a single parameter we don't need to have the brackets
	console.log(a + b);    
	return a + b;  
}
add(34, 35); 
```

```javascript
const multiplyBy2 = number => number * 2;    // for a single parameter and single line functions we don't need to have the brackets
console.log(multiplyBy2(34.5));
```

we can replace previous code with arrow which makes the code more clean and readable

```javascript
[
	'hi',
	'hellow',
	'world'
].forEach((value, index) => {     // arrow makes the code more readable
	if (value === 'hellow'){
	return;    
	}
	console.log(value);
	console.log(index);    
}
);
```

### addEventListener

we can add event listeners for html containers, for the equivalent code for *onclick* we can listen for the click event to happen and execute a function, we can add multiple event listeners for one event and execute multiple functions. since we can add and remove eventListeners it is the best practice to follow.

```javascript
<body>
    <button class="js-button">click</button>
    <script>
        const clickButton = document.querySelector('.js-button');
        clickButton.addEventListener('click', () => {
          console.log('clicked');
        });
    </script>
  </body>
```

> when we want to remove a event listener we have to store the function in a variable because we cannot give the function's string?? 

``` javascript
const clickButton = document.querySelector('.js-button');
const printClick = () => {
	console.log('clicked');
};
const printhellow = () => {
	console.log('hellow, world!');
};
const printHi= () => {
	console.log('hi!');
};

clickButton.addEventListener('click', printClick);
clickButton.addEventListener('click', printhellow);
clickButton.addEventListener('click', printHi);

clickButton.removeEventListener('click', printClick)
```

### Input 

```javascript
document.body.addEventListener('keydown', (event) => {
	console.log(event.key);
});
```

### Filter

takes function as a argument and returns a new array.

```javascript
[1,-3,5].filter((values, index)=> {
	/* if(values >=0){
		return true;
	}else{
		return false;
	}
		*/
	return values >= 0;
});
```

### Map

also returns a new array and takes function as an argument.

```javascript
>[1,1,3].map((value, index) +> {
	return value + 100;        // multiply by 2
});
[11,11,13]

```

> if the function is only one line we can ignore the return and curly brackets. `[1,2,3].map((value, index) => value * 2));` 

### Closure

- if a function has access to a value
- it will always have  access to  that value

```javascript
document. querySe1ectorA11( ' .js-delete-todo-button ' )
	.forEach((de1eteButton, index) => {
	deleteButton.addEventListener( ' click' , () => {
		console. log(index);
		todoList.sp1ice(index, 1);
		renderTodoList();
		});
	});
```

> value gets packaged together/**enclosed** with the function, because of this the value of index once deleted from the scope after that function is executed, when we call the inner function this closure property packages the variable so that there is no error. thus closure encloses the variable to the function once the the function has access to the variable.

## References

[JavaScript Tutorial Full Course - Beginner to Pro](https://youtu.be/EerdGm-ehJQ?si=YiniT8Ii1jJ32Jn6)

