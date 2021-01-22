# Read: 10 - JS Debugging
## JavaScript book, Ch. 10, “Error Handling & Debugging”
- Javascript can be hard to learn and everyone makes mistaks when writing it. This chapter will help you learn how to find the errors in your code. It will also teach you how to write scripts that deal with potiental errors gracefully.
- The console & dev tools: tools built into the borwser that help you hunt for errors.
- Common problems: Cmoon sources of errors, and how to solve them.
- Handling errors: How code can deal with potential errors gracefully.
### The Stack 
- The JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks (or piles) the new function on top of the current task.
### Execution Context & Hosting 
- Each time a script enters a new execution context, there are two phases of activity:
  - 1. Prepare:
    - The new scope is created
    - Variables, functions, and arguments are created
  - 2. Execute:
    - Now it can assign values to variables
    - Reference functions and run their code 
    - Execute statments 
- Understand that these two phases happen helps with udnestand a concept called hoisting, you may have seen that you can:
  - Call functions before they have been declared
  - Assign a valeu to a variable that has not yet been declared
- Each execution context also creates its own variables object.
### Understanding Scope
- In the interpeter, each execution context has its own variables object. It holds variables, functions, and parameters available within it. Each execution contex can also access its parent'ss variables object.
### Understanding Errors
- If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code.
- If you are anticipating that something in your code may cause an error, you can use a set of statements to handle the error.
### Error Objects
- Error objects can help you find where your mistakes are and browsers have tools to help you read them.
- These are JavaScript's seven different types of error objects:
  - Syntax Error
    - Mismatching or Unclosed Quotes
    - Missing Closing Bracket
    - Missing Comma in Array
    - Malformed property name
  - Reference Errors
    - Variable is undeclared
    - Named function is undefined
  - EvalError
    - it is rare that you would see this type of error, as browsers often throw other errors when they are supposed to throw an EvalError.
  - UriError
    - Characters are not escaped in URI's
  - TypeErro
    - Value is unexpected data type
    - Incorrect Case for document object
    - Incorrect case for write() method
    - Method does not exist
    - Dom node does nose exist
  - RangeError
    - Number outside of range
    - Cannot create arrat with -1 items
    - Number of digits after decimal in toFixed() can only be 0-20
    - Number of digits in toPrecision() can only be 1-21
  - Error
    - Genere error object
  - NaN: not a number
### How To Deal With Errors
- Now that you know what an error is and how the browser treats them, there are two things you can do with the errors.
  - 1. Debug the script to fix errors
  - 2. Handle Errors Gracefully
    - You can handle errors gracfully using try, catch, throw, and finally statements.
### A Debugging Workflow
- Debuggin is about deduction: eliminating potential causes of an error. Here is a workflow for techniques you will meet over the next 20 pages. Try to narrow down where the probem might be, then look for clues.
  - Where is the problem?
    - 1. Look at the error message, it tells you.
    - 2. Check how far the script is running.
    - 3. Use breakouts where things are going wrong.
  - Where Exactly is the problem?
    - 1. When you have set breakpoints, you can see if the variables around them have the values you would expect them to. If not, look earlier in the script.
    - 2. Break down / break out parts of the code to  test smaller pieces of the functionality.
    - 3. Check the number of paramter for a function, or the number of items in an array.
### Browser Dev Tools & JavaScript Console
  - The JavaScript Console will tell you when there is a problem with a script, where to look for the problem, and what kind of issue it seems to be.
  - The JavaScript console is just one of several developer tools that are found in all modern browsers.
### How To Look At Erros in Chrome
- The cnosle will show you when there is an error in you JavaScript. It also displays the line where it became a problem for the interpreter.
### Breakpoints
- You can pause the execution of a script on any line using breakpoint. Then you can check the values stored in variables at that point in time.
### Summary
- If you understand execution contexts (which have two stages) and stacks, you are more likely to find the error in your code.
- Debugging is the process of finding errors. It invovles a process of deduction.
- The console helps narrow down the area in which the error is located, so you can try to find the exact items.
- JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.
- If you know that you may get an error, you can handle it gracefully using the try, catch, finally statements. Use them to give your users helpful feedback.
