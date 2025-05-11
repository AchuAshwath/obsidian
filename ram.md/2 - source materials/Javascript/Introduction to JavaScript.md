07-04-2025 10:19:03

Status : #child 

Tags : [[Introduction to JavaScript]] [[Expressions]] [[Operators]] [[Data Types]]

# JavaScript

## [Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types)

 1. can't use special words, like `let` and `const`
 2. can't start with numbers
 3. can't use special characters except `$` and `_`

```javascript
let variable_name = 'value';
```

> let is used to create a new variable, you will run into error if you use it to re-assign a new value to an existing variable. and we cannot create two variables with the same name.

> camelCase is the naming convention of JavaScript.

```javascript
const variable_name = 'value';
```

> best practice to use const when we know we will not change the value of a variable, keeps the code clean

```javascript
var variable_name = 'value';
```

> var has some problems, such that var doesn't really follow the rules of scope... thus we don't use var in new JavaScript code

Totally three ways to create variables in javascript, 
1. let
2. const
3. var

we use const by default, and use let if we have to change the value of the variable.

## [Data Types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Data_structures)

#### Strings

Strings = 'hellow'

Template Strings  => used in Interpolation and multi-line strings => recommended solution for string formatting

```javascript
>`this is math, ${34 + 35}`;
< 'this is math, 69'
```

#### Boolean

Falsy Values in javascript are,
1. false
2. 0
3. '' -> empty string
4. NaN -> not a number, result of improper math
5. undefined -> variable doesn't have a value, undefined shall be explicitly defined using const, but cannot be assigned like let.
6. null
## [Expressions and Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_operators)

comparison operators -> `===` is used for equal to, because `==` tries to convert both values into the same.

```javascript
> console.log(5 == '5.00');
< true

> console.log(5 === '5.00');
< false
```

Ternary operator can be saved as a variable, 

```javascript
> const result = true ? 'truthy' : 'falsy';
< 'truthy'
```

&&(and operator)- **Guard Operator** because && follow *short circuit evaluation*, if the first part of the && is false, it won't check the other part

```javascript
> false && console.log("truthy");
// this is a short cut for a if statement like
// if(condiditon){
	//console.log(something);
// }

> const message = 69 && 'hello';
> console.log(message);
< 'hello'
```

||(or operator) - **Default Operator** also short-circuits, 
```javascript
< const currency = 'EUR' || 'USA';
< console.log(currency);
> 'EUR'

< const currency = undefined || 'USA';
< console.log(currency);
> 'USA'
```

> can be used to moderate a default value, with if condition.
## [Control flow and Error Handling](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling)


If-conditions have scopes, such that a variable declared inside the if condition's scope will be accessible in that scope only.

```javascript
const variable_name = value;

if(some_condition){
	const variable_name = 5;
}

// This is only possible because of the scope nature of javascript.
```

## [Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

functions follow the same rules as naming variables. 

```javascript
function func_name(parameter, defaultParameter = value){
	return parameter * defaultParameter;
}
```

## [Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_objects)

```javascript
const object = value;
const objectCopy = object;
```

In javaScript objects are copy by reference meaning that the objectCopy is not a actual copy of the object, but more of a reference to the object itself.

```javascript
> const product = {
	name : 'socks',
	price : 1090,
	// property : value
	'delivery-time' : '1 day', 
	rating: {    // nested object
		stars : 4.5,
		count :87
	},
	summary : function summary(){
		console.log(`Product name is ${this.name} and the price is ${this.price}. This product will take approximately ${this.['delivery-time']} to be delivered, and it has ${this.rating.stars} stars from ${this.rating.count} reviews.`)
	}
} 

> console.log(product);
> {name: 'socks', price: 1090}
> console.log(product.name);
> socks
> // change objects property value 
> product.name = 'cotton-socks';
> console.log(product.name); // dot notation
> cotton-socks
> // add new property
> product.newProperty = true;
> console.log(product.newProperty);
> true
> console.log(product['delivery-time']); // bracket notation
> '1 day' 
>  console.log(product.rating.count);
>  87
>  
```

> bracket notation is used when there is a error due to the name of the property, such example would be delivery-time, here - is considered as minus sign so hence we can use the bracket notation to overcome this shortcoming.

#### Object Comparison

```javascript
> const object1 ={
	message :'hello',
	message2: 'world!'
}

> const object2 = object1;

> object1.message ='Good job!';    // even though the variable is const, the value inside can be changed but not the reference value.
> 'Good job!'

> console. log(object1);
> {message: 'Good job!', message2: 'world!'}

> console. log(object2);
> {message: 'Good job!', message2 : 'world!'}

> const object3 ={
	message :'Good job!',
	message2 : 'world!'
}

> console.log(object3 === object1)    // object are compared by reference not by value
> false
> console.log(object2 === object1)
> true

```

#### Destructuring and short hand in Javascript

```javascript
const message = object1.message;
// can be re-written as
const { message } = obejct1;
or
const { message, message2 } = object1;    // destructuring

const object = {
	// message : message,
	message,    // short-hand property - shortcut for the above code 
	// method : function functionName(){
	// some code
	// }
	method(){    //short-hand method - shortcut for above code
		console.log('method');
	}
}
```

#### Built-in Objects

1. console
2. Math
3. JSON - JavaScript Object Notation - converts javaScript object into JSON

```JSON
// only use double quotes
{
	"name" : "shirt",
	"delivery-time" : "1 day",
	"rating" : {
		"starts" : 4.5,
		"count" : 87 
	}
}
```

```javascript
> console.log(JSON.stringify(product));
> {"name":"socks","price":1090,"delivery-time":"1 day","rating":{"stars":4.5,"count":87}}
> const jsonString = '{"name":"socks","price":1090,"delivery-time":"1 day","rating":{"stars":4.5,"count":87}}'
> console.log((jsonString));
> 1. {name: 'socks', price: 1090, delivery-time: '1 day', rating: {…}}

1.2. livery-time: "1 day"
2.3. me: "socks"
3.4. ice: 1090
4.5. ting: {stars: 4.5, count: 87}
5.6. Prototype]]: Object


```

> JSON is a universal language, acknowledged by all programming languages, and is used to send data between computers and store data. 

4. localStorage - used to store data in the localstorage, because if the page is refreshed variables will be erased from the memory.

```javascript
localStorage.setItem('score', JSON.stringify(score));    // stores object in local, localStorage only accepts string as arguments

score = (localStorage.getItem('score'));    // retrieve object from local, since the data is stored as string we parse it back to retrive the object

localStorage.removeItem('score');    // remove the saved string from the local storage
```

use default operator to replace a if condition,

```javascript
    // if (localStorage.getItem('score')) {
    //     // console.log('score exists in local storage');
    //     score = JSON.parse(localStorage.getItem('score'));
    // }else{
    //     // console.log('score does not exist in local storage');
    //     score = {
    //         player: 0,
    //         computer: 0,
    //         draw: 0
    //     }
    // }
    //
    // replacement for the above code
    score = JSON.parse(localStorage.getItem('score')) || {
        player: 0,
        computer: 0,
        draw: 0
    };
```

#### Auto-boxing

Javascript automatically warps anything into a special object, for example

```javascript
> typeof 'hello'
'string'
>'hello'.length
5
>'hello'.toUpperCase();
'HELLO'
```

> here the 'hello' is automatically converted into a special object which has the methods and attributes.
## References

[JavaScript Tutorial Full Course - Beginner to Pro](https://youtu.be/EerdGm-ehJQ?si=YiniT8Ii1jJ32Jn6)

