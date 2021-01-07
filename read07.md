# Reading 07 notes: Programming with JavaScript
## Introduction
### How Javascript makes pages more interactive
    * Access Content: You can use JavaScript to select any element, attribute, or text from an HTML page.
    * Javascript allows you to make web pages more interactive by accessing and modifying the content and markup used in a web page while it is being viewed in the browser
    * Modify Content: You can use JavaScript to add elements, attributes, and text to the page, or remove them.
    * Program Rules: You can specify a set of steps for the browser to follow, which allows it to acces or change the content of a page.
    * It can make the web page feel interactive by responding to what the user does
    * React to events: You can specify that a script should run when a specific event has occured.
### Examples of Javascript in the browser
    * Access the content of the page
    * Modify the content of the page
    * Program rules or instructions the browser can folllow
    * React to events triggered by the user
    * Examples: Slideshows, Forms, Reload part of the page, Filtering data
## The abcs of programming 
### What is a script and how do I create one
    * A Script is a series of instructions that a computer can follow to acheive a goal.
    * You could compare them to: Recipes, Handbooks, Manuals
### Writing a script 
    * To write a script, you first need to state your goal then list the tasks that need to be comleted in order to acheieve it 
    * Define the goal
        - First, you need to define the tasks you want to achieve, You can think of this as a puzzle for the computer to solve.
    * Design the Script
        - To design a script you split the goal into a series of taska that are going to be involved in solving this puzzle. This can be represented using a flow chat
    * Code each step
        - Each of the steps needs to be written in a programming language that the computer understands. In our case, this is JavaScript
### Designing a Script
    * Tasks
        - Once you know the goal of your script, you can work out the individual tasks neede to acheieve it. This high-level view of the tasks can be represented using a flowchart.
    * Steps
        - Each individual task may be broken down into a sequence of steps. When you are ready to code the script, these steps can the be translated into individual lines of code.
### From Steps to Code
    * Vocabulary: The words that computers understand
    * Syntax: How you put those words together to create instructions computers can follow
    * You will also need to learn how a computer achieves different types of goals using a programmatic approach
    * Debugging - serveral ways to discover what might have gone wrong
    * Computers solce problems programmtically; they follow series of instructions one after another.
    * Learn to think like a computer
### Defining a goal & designing the script
    * First thing you should do is detial your goals for the script
### Sketching out the tasks in a flow chart
    * Often scripts will need to perform different taks in different situations. You can use flowcharts to work out hwo the tasks git together
    * Flowchart key: Generic step, Event, input and output, decision
### Summary 
    * A script is a series of instructions that the computer can follow in order to achieve a goal
    * Each time the script runs, it might only use a subset of all the instructions
    * Computers approach tasks in a different way than humans, so your instructions must let the computer solve the task programmitcally
    * To approach wiriting a script, break down your into a series of tasks then work out each step needed to complete that task (a flowchart can help).
## Expressions and Operators
### Expressions
    * An expression evaluates into (results in) a single value. Broadly speaking, there are two types of expressions.
    * Expressions that just assign a value to a variable
    * Expressions that use two or more values to return a single value
### Operators
    * Expressions rely on things called Operators; they allow programmers to create a signle value from one or more values
    * Assignment Operators - Assign a value to a variable
    * Arithmetic Operators - perform basic math'
        - Java contains the following mathematical operators: 
             addtion - Adds on value to another
             subtraction - Subtracts one value from another
             division - Divides two values
             multiplication - Multiples two values using an *
             increment - Adds one to the current number
             decremen - Subtracts one from the current number
             modulus - Divides two values and returns the remainder
    * String Operators - Combine two strings
    * Comparison Operators - Compare two values and return true or false
    * Logical Operators - Combine expressions and return true or false
### String operator
    * there is just on string operator: the + symbol. It is used to join the strings on either side
    * can only add variables not strings
## Functions
    * Functions let you group a series of statements together to performa specific task. If different parts of a script repeat the same task, you can reuse the function.
    * When you ask the function to perform a task, it is known as calling a function
    * pieces of information passed to a function are known as paramaters
    * When you write a function and you expect it to provide you with an answer, the response is known as a return value,
### Declaring a function
    * To creat a function, you give it a name and then write the statements needed to achieve its task inside the curly braces. This is known as a function declaration.
### Calling a Function
    * Having declared the function, you can then execute all of the statements between its curly braces with just one line of code.This is known as calling the function.
### Declaring a function 
    * Sometimes a function needs specific information to perform its task. In such cases. when you declare the function you give it parameters. Inside the function, the parameters act like variables
### Calling Functions That need information
    * When you call a function that has parameters, you specify the values it should use in the parenthesis that follow its name. 
    * The values are valled arugments, and they can be provided as values or as variables
    * Arguments as Values 
    * Arguments as Variables
### Getting a single value out of a function
    * some functions return information to the code that called them. For example, when they perform a calculation, they return the result.
