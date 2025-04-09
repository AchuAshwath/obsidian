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
const add = (a, b) => {
	console.log(a + b);    
	return a + b;  
}
add(34, 35); 
```


## References

[JavaScript Tutorial Full Course - Beginner to Pro](https://youtu.be/EerdGm-ehJQ?si=YiniT8Ii1jJ32Jn6)

