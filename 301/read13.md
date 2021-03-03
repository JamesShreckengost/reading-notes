# Read: 13 Update/Delete
## Sending From Data
- Prerequisites: Basic literacy, and understanding of HTMl, and basic knowledge of HTTP and server side programming.
- Objective: To understand what happens when form data is submitted, including getting a basic idea of how data is processsed on the server.
### Client/Server Artchitecture
- a client send a request to a server, using the HTTP protocol. The servser answers the request using the same protocol.
- an HTML form ona web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server. 
### On The Client Side: Defining how to send the data
- The form element defines how the data will be sent. 
- All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. The two most important attributes are action and method.
  - The Action Attribute: defines where the data gets sent. Its value must be a valid relative or absolute URL. 
  - If this attribute isnt provided, the data will be sent to the URL of the page containing the form - the current page.
  - The Method Attribute: defines how data is sent. 
  - The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the get method and the post method.
  - The Get Method: the method ued by the browser to ask the server to send back a given resource: Hey server, I want to get this resource. 
  - The Post Method: the method the browser uses to talk to the server when asking for a response that takes into account the data provided int the body of the HTTP request: Hey server, take a look at this fata and send me back an appropriate result.