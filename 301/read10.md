# Reading 10: The Call Stack
## The call stack defined on MDN
- a mechanism for an interpreter to keep track of its place in a script that calls multiple functions -- what cunctions is currently being run and what functions are called from within that function.
  - When a script call a function, the interpreter adds it to the call stack and the starts carrying out the function
  - Any functtions tha are called by that function are added to the call stack further upm and run where their calls are reached
  - When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
  - If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error
  ### Example:
  ```javascript
  function greeting() {
   // [1] Some code here
   sayHi();
   // [2] Some code here
}
function sayHi() {
   return "Hi!";
}

// Invoke the `greeting` function
greeting();

// [3] Some code here
`
## Understanding the Javascript Call Stack
- The JS engine, is a single-threaded interpreter copmrising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.
- The call stac is primarily used for function invocation. Since the call stack is single, functions execution, is done, one at a timee, from top to bottom. It means the call stack is synchronous.
- The understanding of the call stack is vital to Asynchronous programming.
- In asynchronous JS, we have a callback function, an event loop, and task queue. The callback function is acted upon by the call stack during execution after the call back function has been push to the stack by the event loop.
- At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocatoin(call)
- LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.
- Manage function invocation(call): The call stack maintains a record of the position of each stack frame. It knows the next function to be execeuted(and will remove it after execution). This is what makes code execution in JS synchronous.
### How does the call stack handle function calls?
```Javascript
function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();
```
- When secondFunction() gets executed, an empty stack frame is created. It is the amain entry point of the program.
- secondFunction() then calls and prints "Hello from firstFunction"  to the console.
- firstFunction() returns and prints "Hello from firstFunction" to the console.
- firstFunction() is pop off the stack
- The execution order then move to secondFunction()
- secondFunction() returns and print "The end from SecondFunction" to the console
- secondFunction() is pop off the stack, clearing the memory
### What causes a stack overflow?
- This occurs when there is a recursive function(a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
## Javascript error messages
- Types of error messages
  - Reference error: As simple as when you try to use a variable that is not yet declared you get this type os errors.
  - Syntax error: Occurs when you have something that cannot be parsed in tersms of syntax, like when you try to parse an invalid object using JSON.parse
  - Range errors: Try to manipulate an object with some kend of length and give it an invalid length and this kind of error will show up.
  - Typer Errors: Show up when the tyoes you are trying to use or access are incompatibale, like accessing a property in an undefined typed of variable
  ### Debugging
  - Easiest way to debug your code is in the console.
