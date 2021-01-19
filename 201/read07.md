# Read: 07 - HTML Tables; JS Constructor Functions
## Domain Modeling (Repo in codefellows)
- Domain modeling is the process of creating a conceptual model in code for a specific problem. 
  - A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. 
  - An entity that stores data in properties and encapsulates behaviors in methods is commonly reffered to as an object-oriented model.
  - Have two essential metrics for gauging something 
  - build self-contained objects with the same attributes and behaviors
- Define a constructor and intialize properties
  - To define the same properties between many objects, you'll want to use a constructor function
- Below is a table that summarizes a JavaScript representation of an EpicFailVideo object.
  -|   Property  |    Data      | Type   |
    ---------------------------------
   | epicRating  |    1 to 10   | Number |
   ------------------------------------
   | hasAnimals  | true or false| Boolean |

- Here's an implemenation of the EpicFailVideo constructor function.
```javascript
var EpicFailVideo = function(epicRating, hasAnimals){
  this.epicRating = epicRathing;
  this.hasAnimals = hasAnimals;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail);
console.log(corgiFail);
```
- This is object-oriented programming in JavaScript at its most fundamental level.
  - 1. The new keyword instantiates (i.e. creates) an object.
  - 2. The constructor fucntion intializes properties inside that object using the *this* variable.
  - 3. The object is stored in a variable for later use.

- Math.random() function used to make a random number generator.
```javascript
var EpicFailvideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals
}

EpicFailvideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

var parkourFail = new EpicFailVideo(7, false)
var corgiFail = new EpicFailVideo(4, true)

console.log(parkourFail.generateRandom(1,5));
console.log(corgitFail.generateRandom(1,5));
```
For rest of code look to: [Domain Modeling Repo](https://github.com/codefellows/domain_modeling#domain-modeling)
## Chapter 6: “Tables” (pp.126-145)
- There are several types of information that need to be displayed in a grid or table. For example: sports results, stock reports, train timetables.
### Whats a Table?
- A table represents information in a grid format. Examples of tables include financial reports, TV schuedules, and sports results.
  - Each block in the grid is referred to as a table cell. In HTML a table is written out row by row.
### Basic Table Structure
#### <table>
  - The <table> element is used to crea a table. The contents of the table are written out row by row/
#### <tr>
  - You indicate the start of each row using the opening <tr> tag. (The tr stands for table row.)
  - It is followed by one or more <td> elements (one for each cell in that row.)
  - At the end of the row use a closing </tr> tag.
#### <Td> 
  - Each cell of a table is represented using a <td> element. (The td stand for table data.)
  - At the end of each cell you use a clisng </td> tag.
#### <th>
  - The <th> element is used just like the <td> element but its purpose is to represent the heading for either a column or a row.
### Spanning Columns
- Sometimes you may need the entries in a table to stretch across more than one column
- The colspan attribute can be used on a <th> or <td> element and indicates how many columns that cell should run across
- example: <td colspan="2">Geography</td>
### Spanning Rows
- You may also need entries in a table to stretch down across more than one row.
- The rowspan attribute can be used on a <th> or <td> element to indicate how many rows a cell should span down the table.
- example: <td rowspan="2">Movie></td>
### Long Tables
- There are three elements that help distinguish between the main content of the table and the first and last rows (which can contain differnt content).
- These elements help people who use screen readers and also allow you to style these sections in a differnt manner than the rest of the table.
#### <thead>
- The headings of the table should sit inside the <thead> element.
#### <tbody>
- The body should sit inside the <tbody> element.
#### <tfoot>
- The footer belongs inside the <tfoot> element

## Chapter 3: “Functions, Methods, and Objects” (pp.106-144)
### Creating An Object: Constructor Notation
- The new keyword and the object constructor create a blank object. You can then add properties and methods to the object.
- First, you create a new object using combination of the new keyboard and the Object() constructor function. (This function is part of the JavaScript language and is used to create objects.)
### Updating An Object
- To update the value of properties, use dot notation or square brackets. 
- They work on objects created using literal or contructor notation.
- To delete a property, use the delete keyword.
### Creating Many Obkects: Contructor Notation
- Sometimes you will want several objects to represent similar things.
3- Object constructors can use a function as a template for creating objects.
- First, create the template with the object's properties and method.
- You can create instances of the object using the constructor function.
- The new keyboard followed by a call to the function creates a new object.
- The properties of each object are given as arguments to the function.
### Creating Objects using contructors
- To access a property of this object, you can use dot notation, just as you can with any object.
- For Example, to get the hotel's name you could use hotel.name
### This is a keyword
- The keyword this is commonly used inside functions and objects. Where the function is declared alters what this means. It always regers ti one object, usuallay the object in which the function operates.
- a function in global scope
  - When a function is created at the top level of a script (that is, inside another object or function), then it is in the global scope or global content
  - The default in the content is the window object, so when this is used inside a fucntion in the global context it regers to the window object.
- Global Variables
  - All global variables also become propertues of the window object, so when a function is in the global context, you can access gloabl variables using the window object, as well as its other properties.
- A Method Of an Object
  - When a function is defined inside an object, it becomes a method. In a method *this* refers to the containing object.
- Function Expression As Method
  - If a nmes function has been defined in global scope, and it is then used as a methof of an object, this refers to the object it is contained within.
### Recap: Storing Data
- In javascript, data is represented using name/value pairs. To organize a your data, you can use an array or object to group a set of related values. In arrays and objects the name is also known as a key.
  - Variables: A variable has just one key (the variable name) and one value.
  - Arrays: Arrays can store multiple pieces of information. Each piece of information is seperated by a comma. The order of values is important because items in an array are assigned a number.
- If you want to access items via a property name or key, use an object (but note that each key in the object must be unique). If the order of the items is important, use an array.
### Arrays are objects
- Arrays are actually a special type of object. they hold a related set of key/value pairs (like all objects), but the key for each value is its index number.
- You can combine arrays and objects to create  complex data structures: Arrats can store a series of objects (and remember their order). Objects can also hold arrays (as values of their properties)
### Summary
- Functions allow you to group a set of related statements together that represent a single task.
- Functions can take parameters (information required to do their job) and may return a value.
- An object is a series of variables and functions that represent something from the world around you.
- In an object, variables are kown as properties of the object; functions are known as methods of the object.
- Web browsers implement objects that represent both the browser window and the document loaded into the browser window.
- JavaScipt also has several built-in objects such as String, Number, Math, Date. Their properties and methods offer functionality that help you write scripts.
- Arrays and objects can be used to create complex daata sets (and both can contain the other).