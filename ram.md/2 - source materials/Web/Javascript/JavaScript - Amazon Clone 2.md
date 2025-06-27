23-04-2025 15:16:09

Status : #child

Tags : 

## Backend

- another computer that manages the data of the website

### XMLHttpRequest

- Built in class provided by javascript
- `XMLHttpRequest.open()` - two arguments (method such as GET POST) and URL
- **URL** - Uniform Resource Locator, address for the internet
- **Status Code** 
	- starting with 4 says problem is with us, 5 says problem is with backend (400, 404, 500) - failed
	- starts with 2 (200, 201, 204) - succeeded 
- The list of backend URL paths are known as backend API - application programming interface
- Browser usually sends a GET request to the given URL.
- **Callback** - function to call in the future (setTimeout)

### Promises
- better way to handle asynchronous code
- similar to the done function, 

```javascript
beforeAll((done) => {
	loadProducts(() => {
		done();
	});
});
```

- let's us wait for some code to finish, before going to the next step

```javascript
new Promise((resolve) => {
    loadProducts(() => {
        resolve();
    });
});
```

- similar code to the done function.
- Promise creates a new thread, allowing javascript to  do multiple things at the same time.
- we can send values inside the `resolve(value)` to the next then function as a parameter
- we can run multiple promises at the same time using `promise.all()` and wait for all of them to finish.
-   

**why do we use Promises?**
1. Multiple call backs cause a lot of nesting
2. Promises helps us flatten the code
3. we use `resolve` to wait for the next step

### Fetch 

- better way to make HTTP requests
- fetch uses a promise
- by default fetch will make a GET request
- instead of using a callback to get the response, fetch uses a promise to get the response

```javascript
function loadProductFetch(){
	fetch('http://supersimplebackend.dev/products').then(response) => {
		return response.json();    // asymnchoronous
	}).then((productsData) =>{
		console.log(productsData);
	})
}
```

### Async Await

- even better way to handle asynchronous code
- is a shortcut for promises
- async - makes a function return a promise

```javascript
function loadPage(){}
return new Promise((resolve) => {
	console.log();
	resolve();
})
}

// is equvalent to
async function loadPage() {
	console.log();
}
```

- async makes a function return a promise

```javascript
async function loadPage(){
	console.log();
	return 'value'  // = ersovle('value');
}
loadPage().then((value) => {
	console.log(value);
})
```

**what's the point of async?**
1. aysnc lets us use await
2. await lets us wait for a promise to finish, before going to the next line
3. lets use write asynchronous code like normal code
4. we can only use await, when we're inside a async function.
5. 

```javascript
async function loadPage(){
	console.log('load page');
	await loadProductsFetch();  // = loadProductsFetch().then(() => {})
	return 'value'  // = ersovle('value');
}
loadPage().then((value) => {
	console.log('next step');
	console.log(value);
})

// output
//load page
// load products
// next step
// value
```

![[Pasted image 20250610104840.png]]

- for awwait, the closest function has to be async

```javascript
async function outterFunction(){
	console.log('hello');
function innerFunction() { // we have to make this async 
	await loadProductsFetch();
	}
}
```

- resolve value is returned, so that we can save it to a variable.

```javascript
async function loadProducts() {
  try {
    products = await fetchProducts();
    renderProducts();
  } catch (error) {
    console.error('Error fetching products:', error);
  }
}
```

### Error Handling

- error handling using callbacks, we listen for the error event

```javascript
xhr.addEventListener('error',  (error) => {
	console.log('unexpected error. Please try again later' + error);
});
```

- handling errors in promises, we use catch and then

```javascript
export let products = []; 

export function loadProducts(renderProductsFunction){
const xhr = new XMLHttpRequest();

xhr.addEventListener('load', () => {
    products = JSON.parse(xhr.responseText).map((productDetails) => {
     if(productDetails.type === 'clothing'){
       return new Clothing(productDetails);
     };
     return new Product(productDetails);
   }).catch((error) => {
	   console.log('Unexpected Error, Please try again later' + error)
   });
   renderProductsFunction();
 });

 xhr.open('GET', 'https://supersimplebackend.dev/products');
 xhr.send();
```

- handling error in async await, we will use try and catch

```javascript
async function loadProducts() {
  try {
    products = await fetchProducts();
    renderProducts();
  } catch (error) {
    console.error('Error fetching products:', error);
  }
}
```

- we use try/ catch to handle unexpected errors, because our code is correct, but something outside of our control is involved.
- we can manually create error using the `throw` keyword
- throw doesnt not work in the future, that means we can't use it inside a code that will be executed in the future, so promises provide a argument called reject to create an error in the future

```javascript
const value = await new Promise((resolve, reject) => {
	loadCart(() => {
		reject('error');
		resolve('value');
	});
});

catch (error) {
	console.log('Enexpected error!');
}
```

> we use reject to throw an error asynchronously, and we use throw when we are throwing an error synchronously.


#### Types of Request
1. GET - get something from the backend
2. POST - create something, lets us send data to the backend
3. PUT - update something
4. DELETE - delete something

**window.location.href** -change the url at the top

URL parameter - we can put some data into URL and then we can use that data from the URL in javascript


