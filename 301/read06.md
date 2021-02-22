# Read: 06 - Node, Express, and APIs
## What is nodeJS
- The v8 engine is the open-source JavaScript engine that runs in google chrome and other Chromium-based web browsers. 
- Designed for performance and responsible for compiling Javascript directly to native machine code.
- can use to execute Javascript on our computers
- Node is built on google chrome's v8 javascript engine
  - The v8 engine is the open source Javascript engine that runs in google chrome and other chromium-based web browsers.
### Node binaries vs Version manager
- Version manager is a program that allows you to install multiple versions of Node and switch between them at will.
- One advantage is that it negates potiental permission issues when using Node with npm and lets you set a Node version on a per-project basis.
- node -v to check if installed
### 
Node.js has Great support for modern javscript
- You can write your JS using the latest and most modern syntax
- You dont generally have to worry about compatbility issues 
```Javascript
function upcase(strings, ...values) {
  return values.map(name => name[0].toUpperCase() + name.slice(1))
    .join(' ') + strings[2];
}

const person = {
  first: 'brendan',
  last: 'eich',
  age: 56,
  position: 'CEO of Brave Software',
};

const { first, last } = person;
const emoticon = [ ['┌', '('], ['˘', '⌣'], ['˘', ')', 'ʃ'] ];

console.log(
  upcase`${first} ${last} is the creator of JavaScript! ` + emoticon.flat().join('')
);
```
- Npm, the Javascipt package manager has over 1,000,000 packages of JS code avaiable to download.
- Install package globally
- Install package locally
- Node-modules folder is where npm has saved lodash and any libraries tat lodash depends on
- In the package.json file, youll see lodash under the dependencies field. This allows any dev anywhere to clone your project and use npm to install whatever packages it needs to run
### What is Node.js used for?
- USed for anything from bundling your Js files and dependencies into static assets, to running tests, or automatic code linting and style checking.
- Run Js on the server
- MOde is event-driven, which means that everything that happens in Node is in reaction to an event.
- Node.js has a built-in module to help you implement a cloning strategy on a single server

### Nodes execution model:
- Node apps pass async taks to the event loop, along with a callback
- The event loop efficiently manages a thread pool and executes tasks efficiently...
- ... and executes each callback as taks complete
### Conclusion
- Node is a vast and expansive subject.
- Node is an event-basedm non-blocking, asynchronous I/O runtime that uses google's v8 JS engine and libuv library.
Source: [Node.js](https://www.sitepoint.com/an-introduction-to-node-js/)