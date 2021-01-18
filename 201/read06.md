# Read: 06 - JS Object Literals; The DOM
## Chapter 3: “Object Literals” (pp.100-105)
### What is an object?
- Objects group together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on new names.
  - In An Object Variables Becomes Known As Properties
  - if a variable is part of an object, it is called a property. Properties tell us about the object, such as the name of a hotel or the number of rooms it has.
- In an object: Functions Become Known As Methods
  - If a function is part of an object, it is called a method. 
  - Methods represent taks that are associated with the object.
- This object represents a gotel. It has five properties and one method. The object is in curly braces. It is stored ina variable called hotel 
- Like variables and named functions, properties and methods have a name and a value. In an object that name is called a key. 
- The value of a property can be a string, number, Boolean, array, or even another object. The value of a method is always a function.
- Objects consist of a set name/ value pairs.
### Creating An Object: Literal Notation
- Literal Notation is the easiest and most popular way to creat objects. (There are several other ways to create objects.)
  - The object is the curly braces and their contents. The object is soted ina variable called hotel. So you would refer to it as the hotel object. 
  - Seperate each key from its value using a colon. Seperate each property and method witha comma (but not after the last value).
  - In the checkAvailability() method, the this keyword is used to indicate that it is using the rooms and booked properties of this object.
  - When setting properties, treat the values like you would do for variables: string live in qoutes and arrays live in square brackets.
### Accessing An Object and Dot Notation
  - You can access the properties or methods of an object using dot notation. You can also access properties using square brackets. 
  - To access a property or method of an object you use the name of object, followed by a period, then the name of the property or methof you want to access. This is called dot notation.
  - The period is known as the member operator. The property or method on its right is member of the object on its left. Here, two variables are created to hold the hotel name and number of vacant rooms.
  - You can also access the properties or methods of an object using square bracket syntax. This time the object name is followed by square brackets, with the property or method inside them.
  - This notation is most commonly used when:
    - The name of the property or method contains special characters (such as a dash).
    - The name of the property is a number (technically allowed, but should generally be avoided)
    - A variable is being used in place of the property name (you will see this technique used in Chapter 12)
## Chapter 5: “Document Object Model” (pp.183-242)
  - The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window. 
  - The DOM is neither part HTML, nor part of JavaScript; is it a seperate set of rules.
  - The DOM specifies the way in which the browser should this model using a DOM tree.
  - Each object represents a different part of the page loaded in the browser window.
  - You will hear people call the DOM an Application Programming Interface (API): User interfaces let humans interact with programs; APIs let programs (and scripts) talk to each other. The DOm staes what your scripts can ask the browser about the current page, and how to tell the browser to update what is being shownto the user.
### The DOM Tree Is A Model Of A Web Page
- As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browsers memory, it consists of four main types of nodes
- Each node is an object with methods and properties. Scripts access and update this DOM tree (not the source HTML file). Any Changes made to the DOM tree are reflected in the browser. 
- The Document Node
  - Every element, attribute and piece of text in the HTML is represented by its own DOM node. At the top of the tree a document node is added: it represents the entire page
- Element Node 
  - This is why you star by learning methods that allow you to access element nodes, before learning to access and alter text or attributes.
- Attribute Nodes
  - The opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree. Attribute nodes are not children of the element that carries them; they are part of that element.
- Text Nodes
  - Once you have accessed an element node, you can reach the text within that element. This is stored in its own text node. Text nodes cannot have children. If an element contains text and another child element, the child element is not a child of the text node but rather a child of the containing element
### Working With The DOM Tree
- Accessing and updating the DOM tree involces two steps:
  - 1. Locate the node repesents the elemtn you want to work with
  - 2. Use its text content, child elements, and attributes
- The terms elements and element nodes are used interchangeably but when people say the DOM is working with an element, it is an actually working with a node that represents that element.
- Step 1: Access The Elements: Select an individual element node, select mulitple elements, tranversing between element nodes
- Step 2: Work with those Elements: Access/Update text node, work with html content, acess or update attribute values
### Caching DOM Queries 
- Methods that find elemetns int the DOM tree are called DOM queries. When you need to work with element more than once, you should use a variable to store the result
- When people talk about storing elements in variables, they are really storing the location of the element(s) within the DOM tree in a variable. The properties and methods of that element node work on the variable.
### Accessing Elements
- DOM queries may return one element, or they may return a NodeList, which is a collection of nodes
- Groups of element nodes
  - If a method can return more than one node, it will always return a NodeList, which is a collection of nodes.
- Methods that returns a single element node:
  - getElementById('id')
  - querySelector('css selector)
- Methods That Return One Or MOre Elements 
  - getElementsByClassName('class')
  - getElementsByTagName('tagName')
  - querySelectorAll('css selector')
### Methods That Select Individual Elements
- getElementById() and querySelector() can both search an entire documents and return individual elements. Both use a similar syntax.
### Nodelists: DOM Queries That Return More That One Element
- When a DOM method can return more than one element, it returns a NodeList
- Live & Static Nodelists
  - In a live NodeList, when your script updates the page, the NodeList is update at the same time.
  - In a static NodeList when your script updates the page, the NodeList is not updated to reflect the changed made by the script
- Here you can see four different DOM queries that all return a NodeList. For each query, you can see the elements and their index numbers in the NodeList that is returned.
### Selecting an element from a nodelist
- There are two ways to select an element from a NodeList: the item()  method and array syntax. Both require the index number of the element you want
- Nodelists have a method called item() which will return an individual node from the NodeList
- Array syntax is preferred over the item() method becuase it is faster. Before selecting a node froma NodeList, check that it contains nodes. If you repeatedly ue the NodeList, store it in a variable.
### Repeating Actions For an Entire Nodelist
- When you have a NodeList, you can loop through each node in the collection and apply the statements to each.
### Traversing The DOM
- When you have an element node, you can select another element in relation to it using these five properties. This is known as tranversing the DOM.
### Whitespace Nodes
- Transversing the Dom can be difficult because some browsers add a text node whenever they come across whitesapce between elements.
### Summary 
- The browser represents the  page using DOM tree.
- DOM trees have four types of nodes: document nodes, element nodes, attribute nodes, and text nodes.
- You can select element nodes by their id or class attributes,  by tag name, or using CSS selector syntax.
- Whenever a DOM query can return more than one node, it will always return a NodeList.
- From an element node, you can access and update its content using properties such as texContent and innerHTML or using Dom manipulation techniques
- An element node can contain multiple text nodes and child elements that are sibling of each other.
- In older browsers, implementation of the DOM is inconsisent (and is popular for using JQUERY).
- Browsers offer tools for viewing the DOM tree.
