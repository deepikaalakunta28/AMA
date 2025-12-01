### QUESTIONS
- What are examples of higher order function?
- What is asynch JS ?
- JS is client side or server side ?
-  What is limit in SQL?
-  What is map method in JS?
- Diff b\w class and id in CSS?
-  What is closures in JS?
- Diff b\w global scope, function scope, block scope?
- What is function in JS?
- Ways to create variables in JS?
- What is hoisting in JS?
- What is callback function?

###  What are examples of higher order function?
Higher-order function = a function that takes another function as an argument or returns a function.
Examples in JavaScript:
```
map()
filter()
reduce()
forEach()
setTimeout()
```
Functions that return other functions
### What is asynch JS ?
Asynchronous JavaScript allows code to run without blocking the main thread.
It lets JS handle tasks like API calls, timers, and file loading while the rest of the code continues to run.
Used with:
- Callbacks
- Promises
- async/await
Async = non-blocking.
### JS is client side or server side ?
JavaScript is both:
- Client-side: Runs in browsers (default use).
- Server-side: Using Node.js, JS can run on servers.
### What is LIMIT in SQL?
LIMIT is used to restrict the number of rows returned by a SQL query.
Example:
```
SELECT * FROM students LIMIT 5;
```
### What is the map() method in JS?
map() creates a new array by applying a function to each element of an existing array.

Example:
```
const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2);
console.log(doubled); 
```
###  Difference between class and id in CSS?
| Feature     | **Class**                      | **ID**                          |
| ----------- | ------------------------------ | ------------------------------- |
| Usage       | Used for **multiple** elements | Used for **one unique** element |
| Selector    | `.classname`                   | `#idname`                       |
| Reusability | Reusable                       | Not reusable                    |
| Specificity | Lower                          | Higher                          |

### What are closures in JS?
A closure is when a function remembers the variables from its outer scope, even after that outer function has finished executing.

Example:
```
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  }
}

const counter = outer();
counter(); // 1
counter(); // 2
```
inner() remembers count → closure.
###  Differences between global, function, and block scope?
**Global Scope**
Accessible everywhere in the program.

Variables declared outside any function or block.

**Function Scope**

Accessible only inside a function.

Created using var, let, or const inside a function.

**Block Scope**

Accessible only inside { } (if, loops, etc.)

Created using let and const.

var does NOT have block scope.
###  What is a function in JS?
A function is a reusable block of code that performs a specific task.
Example:
```
function greet() {
  console.log("Hello!");
}
```
###  Ways to create variables in JS?

Three ways:
- var → old, function-scoped
- let → modern, block-scoped
- const → block-scoped, cannot be reassigned
### What is hoisting in JS?
Hoisting means JavaScript moves variable and function declarations to the top of their scope before execution.
Example:
```
console.log(x); // undefined
var x = 10;
```
But with let and const, accessing before declaration gives an error.
### 12. What is a callback function?

A callback is a function passed as an argument to another function and executed later.

Example:
```
function greet(name, callback) {
  console.log("Hi " + name);
  callback();
}

greet("Deepika", () => console.log("Callback executed"));
```


