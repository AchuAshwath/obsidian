23-04-2025 15:16:09

Status : #child

Tags : 

## Main Idea of JavaScript

1. Save the data
2. Generate  the HTML
3. Make it interactive

While attaching *source for javascript files* the **order** of them is important.

In order to add products to the cart, we can use the `push` method, but which product to add?
To counter this we use something called the **Data Attribute**

Syntax rules of Data Attribute
1. Just an HTML attribute
2. They have to start with data- 
3. example : `data-product-name = ""`

> words separated by `-` is called as kebab case. 

```javascript
<button class="add-to-cart-button button-primary js-add-to-cart" data-product-name = "${product.name}">
	Add to Cart
</button>

document.querySelectorAll('.js-add-to-cart')
    .forEach((button) =>{
       button.addEventListener('click', () =>{
        console.log(button.dataset);
       }) 
    })

> DOMStringMap {productName: 'Adults Plain Cotton T-Shirt - 2 Pack'} 
```

> note that the data-attribute-name is converted from kebab case to camel case - data, if `data-any-name` is used as the name of the attribute then `anyName` would be the attribute name of the dataset for that particular value.

```javascript
document.querySelectorAll('.js-add-to-cart')
    .forEach((button) =>{
       button.addEventListener('click', () =>{
        console.log(button.dataset.productName);
       }) 
    })

> Adults Plain Cotton T-Shirt - 2 Pack
```
 

## Modules

```html
  <script src="data/cart.js"></script>
  <script src = "data/products.js"></script>
  <script src = "scripts/amazon.js"></script>
```

This is just combining all the scripts into a one single big file, that means we can't have variables with same names, this causes naming conflict.

While using scripts tags, its really hard to tell what names are already been used.

So if we want to use only one script and then we will face a problem with unorganized code, then modules will help you to organize the code by importing and exporting variables.

Steps to to get a variable out of a file

1. Add `type="module"` attribute
```html 
//amazon.html
  <script type = "module" src = "scripts/amazon.js"></script>
```

2. Export
```javascript
//go to file data/cart.js
export const cart = [];
```

3. Import
```javascript
// go to file scripts/amazon.js
// import { variables, } from 'directory'
import { cart } from '../data/cart.js';
import { products } from '../data/products.js';
```

> when we use modules we don't have to worry about the order of import, but import must be at the top of the file.

### Remove from DOM

```javascript
// have a identifiable class name in the html
const cartItemContainer = document.querySelector(`.js-cart-item-container-${button.dataset.productId}`);
cartItemContainer.remove();
```

### External Libraries 

External libraries are added into our javascript backend using and these external libraries are compressed by the process of *minification* 

```html
<script src = "https://unpkg.com/dayjs@1.11.10/dayjs.min.js"></script>
```

> again here the external library is loaded directly into page, this might again produce naming conflicts so we shall use modules here too. this is achieve using **ESM Version - EcmaScript Modules** = Javascript, a version that works with javascript modules

```javascript
import dayjs 'https://unpkg.com/dayjs@1.11.10/esm/index.js';
```

> if you check the code in the index.js in the esm version of dayjs, the dayjs object is exported using the default keyword `default export dayjs;`
> normal export with { } are called as named exports.

**default export** - is used when we want to export only one thing from the module. It is best thought that it is better to export only one thing from a module because it makes the code much cleaner.

```javascript
> console.log(dayjs());

1. M {$L: 'en', $d: Tue Apr 29 2025 12:22:45 GMT+0530 (India Standard Time), $y: 2025, $M: 3, $D: 29, …}

2. $D: 29
3. $H: 12
4. $L: "en"
5. $M: 3
6. $W: 2
7. $d: Tue Apr 29 2025 12:22:45 GMT+0530 (India Standard Time) {}
8. $isDayjsObject: true
9. $m: 22
10. $ms: 286
11. $s: 45
12. $x: {}
13. $y: 2025
14. [[Prototype]]: Object
```

**dayjs**

```javascript
const today = dayjs();
const freeDeliveryDate = today.add(7, 'day').format('dddd, MMMM D');
const paidDeliveryDate1 = today.add(4, 'day').format('dddd, MMMM D');
const paidDeliveryDate2 = today.add(2, 'day').format('dddd, MMMM D');

> console.log(freeDeliveryDate, paidDeliveryDate1, paidDeliveryDate2);

Tuesday, May 6 Saturday, May 3 Thursday, May 1
```

### MVC - Model View Controller (Design Pattern)

1. Update the data
2. Regenerate the HTML

In **MVC** we split our code into three parts,
1. **Model** - saves and manages data, code inside the data folder
2. **View** - takes all the data and displays in the DOM, example: amazon.js and checkout.js
3. **Controller** - runs some code if we interact with the page and updates the model, example: event listeners 

## Testing

1. Basic test case - tests if the code works
2. Edge test case - test values that are a little tricky or scenarios where our code can't handle

```javascript
import { formatmoney } from "../scripts/utils/money.js";


// bsasic test cases for formatmoney function
if(formatmoney(1000) === '$10.00') {
    console.log("test passed: formatmoney function works correctly for 1000 cents.");
}else { 
    console.log("test failed: formatmoney function does not work correctly for 1000 cents.");
}

// edge test cases for formatmoney function
if(formatmoney(0) === '$0.00') {
    console.log("test passed: formatmoney function works correctly for 0 cents.");
}
else { 
    console.log("test failed: formatmoney function does not work correctly for 0 cents.");
}

if(formatmoney(2000.5)=== '$20.01') {
    console.log("test passed: formatmoney function works correctly for 20005 cents.");
}
else { 
    console.log(formatmoney(2000.5));
    console.log("test failed: formatmoney function does not work correctly for 20005 cents.");
}

if(formatmoney(2000.4) === '$20.00') {
    console.log("test passed: formatmoney function works correctly for 2000.4 cents.");
}
else { 
    console.log("test failed: formatmoney function does not work correctly for 2000.4 cents.");
}
```

automated test is nothing but using code to test code.
automated tests like these help us set test cases and then test the function every time after there has been a change in the formatMoney function.

group of related test is call the **test suite**

#### Testing Frameworks

Testing frameworks simplify these,
1. create test suites
2. create tests
3. compare values and display result

**Jasmine** - most testing frameworks are similar such as Jest(for Reactjs) and MochaJs 
- spec = test

```javascript
describe(description, specDefinitions)
Create a group of specs (often called a suite).
Calls to describe can be nested within other calls to com ose our suite as a tree.
```

```javascript
it(description, testFunction-opt, timeout-opt )
Define a single spec. A spec should contain one or more expectations that test the state of the code.
A spec whose expectations all succeed will be passing and a spec with any failures will fail. The name it is a pronoun for the test target, not an abbreviation of anything. It makes the spec more readable by connecting the function name it] and the argument description as a complete sentence.
```

> **Best practice**  
> - Test each condition of an if statement as separate test cases, this is know as test coverage
> - **Test Coverage** - how much of the code is being tested - we try maximize test coverage

**Flaky Test** - test that passes sometimes or fails sometimes, this might be due to the usage of localStorage.
**Mocks** - lets us replace a method with a fake version.

```javascript
// spyOn(object, 'method');
spyOn(localStorage, 'getItem');
```

#### Unit test

```javascript
it('add a new product to the cart', () => {        
// mocking the cart localStorage to get consistent results
	spyOn(localStorage, 'setItem');
	
	spyOn(localStorage, 'getItem').and.callFake(() => {
		return JSON.stringify([]);
	});
	
	console.log(cart)
	addToCart("e43638ce-6aa0-4b85-b27f-e1d07eb678c6", 1);
	
	expect(cart.length).toEqual(1);
	expect(localStorage.setItem).toHaveBeenCalledTimes(1);
	expect(cart[0].productId).toEqual("e43638ce-6aa0-4b85-b27f-e1d07eb678c6");
	expect(cart[0].productQuantity).toEqual(1);
});
```

> test case can have more than one expect and will pass only if all the expect cases are satisfied. 


### Object Oriented Programming

- so far we have only used procedural programming - set of step by step instructions using functions.
- Object oriented programming  - use object to structure all of our code
- Object oriented programming represents real world
- For object oriented programming, we will use PascalCase for the naming convention.
- Class is a object generator
- **Constructor** - should use the exact name and don't return anything
- `#` - use it to make any property of the class to be private.'
- we can use inheritance using the `extends` keyword
- we can inherit all the properties and the methods from the parent class using `super` keyword
- we can define a variation of the method inherited by overriding it

```javascript
class Clothing extends Product{
  sizeChartLink;

  constructor(productDetails){
    super(productDetails);
    this.sizeChartLink = productDetails.sizeChartLink;
  }

  extraInfoHTML(){     // override the extraInfoHTML method from the parent class
    // super.extraInfoHTML()  ->  will return the extra info html from the parent class
    return `<a href="${this.sizeChartLink}" target="_blank">Size Chart</a>`;
  }
}
```

> This is really useful because, we don't have to write ternary or if statements, in order to generate different html for different types of products.

```javascript
${product.extraHTML()}
```

- This is polymorphism, objects of child classes can behave differently contained by a parent class

> Originally in javascript this = windows, when they released Javascript Modules, inside a module, this = undefined

```javascript
const obejct = {
	a: 1
	b : this.a
}
// error undefined, because there is no object to point to for this, becayse the obejct has not been created yet.
```

> hence we can conclude that, inside a method this will point to the obejct, and outside the method it will be undefined.

```javascript
function logThis(param1, param2){
	console.log(this+param1+param2); // undefined
}
logThis();    // will print undefined in the console
logThis.call('hello world', 'program', 'javascript');  // will print hello world in the console
// every function has this method called call, which can get a value as an argument which will be stored in this
```

> this keeps the value that it has outside of an arrow function too, That means Arrow functions do not change the value of "this" 

1. Inside a method. this points to the outer object
2. Inside a function, this = undefined, But we can change it using call
3. Arrow functions, do not change the value of "this"







## References




