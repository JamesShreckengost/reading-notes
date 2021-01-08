# Read 08 notes: Operators and Loops
## Comparsion and logical operators 
### Comparison operators evaluating conditions
    - You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a boolean: true or false.
    - Is equal to (==)
        * This operator compares two values ( numbers, strings, or booleans) to see if they are the same
    - Is not equal to (!=)
        * This operator compares two values to see if they are not the same.
    - Strict Equal to (===)
        * This operator compares two values to check that both the data type and value are the same
    - Stick not equal to (!==)
        * This operator compares two values to check that both the data type and value are not the same
    - Greater than (>)
        * This operator checks if the number ont the left is greater than the number on the right
    - Less Than (<)
        * This operator checks if the number on the left is less than number on the right
    - Greater than or equal to (>=)
        * Thhis operator checks if the number on the left is greater than or equal to the number on the right
    - Less than or equal to (<=)
        * This operator checks if the bumber ont the left is less than or equal to the nu,ber on the right.
### Structuring comparison operators
    - In any condition, there is usually one operator and two operands
    - The operands are places on each side of the operator 
    - They can be values or variables. You often see expressions enclosed in parentheses
### Logical Operators
     - Comparison operators usually return single values of true and false
     - Logical operators allow you to compare the results of more than one comparison operator
     - Logical and (&&)
        * This operator tests more than one condition
     - Logical or (||)   
        * This operator tests at least one condition
     - Logical Not (!)
        * This operator teakes a single Boolean value and inverts it
     - Short-Circuit Evaluation
        * Logical expressions are evaluated left to right
        * If the first condition can prvide enought informatioion to get the answer, then there is no need to evaulate the second condition
## For and while loops pgs170-173,176
### Loops
    - Loops check a condition. If it returns it true, a code block will run. Then the condition will be checked again and if it still return true, the code block will run again. It repeats until the condition return false. There are three common types of loops
        * For: If you need to run code a specific number of times, use a for loop. (It is the most common loop.) In a for loop, the condition is usually a counter which is used to tell how many times the loop should run.
        * While: If you do not know how many times the code should run, you can use a while a loop. Here the condition can be something other than a a counter, and the code will continue to loop for as long as the condition is true.
        * Do while: The do...while loop is very similar to the while loop, but has one key difference: it will always run the statments inside the curly braces at least once, even if the condition evaluates to false.
### Loop counters
    - A for loop uses a counter as a condition. This instructs the code to run a specific number of times. Here you can the condition is made up of three statements.
        * Initialization: Create a variable and set it to 0. This variable is commonly called i, and it acts as the counter.
        * Condition: The loop should continue to run until the counter reaches a specified number.
        * Update: Every time the loop has run the statements in the curly bracs, it adds one to the counter.
### Looping 
    - The first time the loop is run, the variable i (the counter) is assigned a value of zero.
    - Every time the loop is run, the condition is checked. 
    - Then the code inside the loop (the statements between the curly brackets) is run.
    - The variable i can be used inside the loop.
    - When the statemtns have finished, the variable i is incremented by 1.
    - When the condition is no longer true, the loop ends. The script moves to the next line of code.
### Using While Loops

        

