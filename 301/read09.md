# Read 09 Notes: Refactoring
## Functional Programming Concepts
- "Complexity is anything that makes software hard to understand or to modify" - John Outerhout
### What is Functional Programming
- a programming paradigm -- a style of building the structure and elements of computer programs -- that treats copmutation as the evaluation of mathematical function and avoids changing-state and mutable data
### Pure Functions
- It returns the same result if given the same arguments 
- It does not cause any observable side effects
- It returns the same result if given the same arguments
- Any fucntion that relies on a random number generator cannot be pure.
- mutability is discouraged in functional programming
- To make the global object pure return the value increased by one.
### Pure function benefits
- Given a parameter A -> expect the function to return value B
- Given a parameter Z -> expect the function to return value D
- We recieve  the numbers array, use map incrementing each number, and return a new list of incremented numbers
### Immutability
- Its state cannot change after it is created.
- You must create a new object with the new value
- We can use reduce to implement this function. 
- trim: removes whitespace from both ends of a string
- split and join: replaces all instances of match with replacement in a given string
- combine these four functions and we can "slugify" our string
### Referential transparency
- pure functions + immutable data = referential transparency
### Functions as first-class entities
- refer to it from constans and variables
- pass it as a parameter to other functions
- return it as result from other functions
### Higher-order functions
- takes one or more functions as arguments, or
- returns a function as its result
## Refactoring Javascript for Readability 
### Scenario 1
```javascript
const URLstore = [];

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  URLstore.push({[rndName]: URL});
  return rndName;
}

function getLong(shortURL) {
  for (let i = 0; i < URLstore.length; i++) {
    if (URLstore[i].hasOwnProperty(shortURL) !== false) {
      return URLstore[i][shortURL];
    }
  }
}
```
```javascript
const URLstore = new Map(); // Change this to a Map

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  // Place the short URL into the Map as the key with the long URL as the value
  URLstore.set(rndName, URL);
  return rndName;
}

function getLong(shortURL) {
  // Leave the function early to avoid an unnecessary else statement
  if (URLstore.has(shortURL) === false) {
    throw 'Not in URLstore!';
  }
  return URLstore.get(shortURL); // Get the long URL out of the Map
}
```

### Scenario 2
```javascript
const friendlyWords = require('friendly-words');

function randomPredicate() {
  const choice = Math.floor(Math.random() * friendlyWords.predicates.length);
  return friendlyWords.predicates[choice];
}

function randomObject() {
  const choice = Math.floor(Math.random() * friendlyWords.objects.length);
  return friendlyWords.objects[choice];
}

async function createUser(email) {
  const user = { email: email };
  user.url = randomPredicate() + randomObject() + randomObject();
  await db.insert(user, 'Users')
  sendWelcomeEmail(user);
}
```
```javascript
onst friendlyWords = require('friendly-words');

const generateURL = user => {
  const pick = arr => arr[Math.floor(Math.random() * arr.length)];
  user.url = `${pick(friendlyWords.predicates)}-${pick(friendlyWords.objects)}` +
    `-${pick(friendlyWords.objects)}`; // This line would've been too long for linters!
};

async function createUser(email) {
  const user = { email: email };
  // The URL-creation algorithm isn't important to this function so let's abstract it away
  generateURL(user);
  await db.insert(user, 'Users')
  sendWelcomeEmail(user);
}
```
### Strategies
```javascript
function showProfile(user) {
  if (user.authenticated === true) {
    // ..
  }
}

// Refactor into ->

function showProfile(user) {
  // People often inline such checks
  if (user.authenticated === false) { return; }
  // Stay at the function indentation level, plus less brackets
}
// =========================================
function searchGroups(name) {
  for (let i = 0; i < continents.length; i++) {
    for (let j = 0; j < continents[i].length; j++) {
      for (let k = 0; k < continents[i][j].tags.length; k++) {
        if (continents[i][j].tags[k] === name) {
          return continents[i][j].id;
        }
      }
    }
  }
}

// Refactor into ->

function searchGroups(name) {
  for (let i = 0; i < continents.length; i++) {
    const group = continents[i]; // This code becomes self-documenting
    for (let j = 0; j < group.length; j++) {
      const tags = group[j].tags;
      for (let k = 0; k < tags.length; k++) {
        if (tags[k] === name) {
          return group[j].id; // The core of this nasty loop is clearer to read
        }
      }
    }
  }
}
Check for Web APIs before implementing your own functionality:
function cacheBust(url) {
  return url.includes('?') === true ?
    `${url}&time=${Date.now()}` :
    `${url}?time=${Date.now()}`
}

// Refactor into ->

function cacheBust(url) {
  // This throws an error on invalid URL which stops undefined behaviour
  const urlObj = new URL(url);
  urlObj.searchParams.append('time', Date.now); // Easier to skim read
  return url.toString();
}
```