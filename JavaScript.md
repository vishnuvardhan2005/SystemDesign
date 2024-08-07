## Variables
There are 3 ways to define variables in JS  
var  
let  
const  
var is function scoped  
let and const are block scoped  
const cannot be re-assigned  

## Data types
### Primities  
  Number  
  String  
  Bool  
  Undefined - no value assigned  
  Null  
  Symbol  
  BigInt  

### Object types  
  Object  
  Array  

In JS anything aprt from primitives is an Object  
```
var person = { name : "Bhagat", age: 8 }  
// access  
person.name  
person["name"]  
person["school"] = "vikas"
del person.age
```

Objects can have methods
```
let person = {
  name : "alexa",
  age : 10,
  greet : function() {return "hello world"}
}
person.greet()
```

nums = [1,2,3,4,5]
nums[0] // first element

// operations on array
push()  
pop()  
slice()  
unslice()
forEach()  
map() // creates a new array with result of provided func exected on every element   
filter()  
```


nums = [1,2,3,4,5]
nums.push(6) // 1 2 3 4 5 6
nums.pop // 1 2 3 4 5
nums.shift() // 2 3 4 5
nums.unshift(1) // 1 2 3 4 5

nums.forEach(n => console.log(n)) // logs all nums
const squares = nums.map( n => n**2)
const even_nums = nums.filter(n => n %2 == 0)
```

## Functions
Functions are reusable blocks of code. Most fundamental building blocks of JS

### Function declaration
```
function doSomething() {
}
```

### Function equation
```
const func = function doSomething() {
}
```

### Arrow functions
```
const func = (params) => {body}
```
If only 1 parameter, () can be removed
If only 1 return {} and return can be removed
```
const f = name => "hello " + name
```

## Asynchronous JS and Promises
JS is single threaded. Asynchronous programming in JS helps us to execute tasks separately so that main thread is not blocked  

### Promise
A promise in JS is an object which represents eventual completion / rejection  
Its like a lottery ticket. We buy a lottery ticket. Later lottery is drawn and if we win, we get the prize.  

```
// Creating a Promise
const promise = new Promise((resolve, reject) => {
  // do some async work
  if (success) {
      resolve("success");
  } else {
      reject("failure");
  }
})

// How to consume a promise
promise
.then(result => console.log(result)) // Promise fulfilled
.catch(err => console.error(err)) // Promise failed or rejected
```

### Async/Await
We can chain then() to consume promises. This chaining can lead to confusing code sometimes
Async, await helps us to use Promises in an easier way. Note internaly they use then()

````
const fun = async function() {
  try {
     const result = await promise
     console.log(result)
  } catch (e) {
      console.error(error)
  }
}
fun()
```

