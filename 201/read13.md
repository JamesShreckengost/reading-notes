# Read: 13 - Local Storage
## “The Past, Present, and Future of Local Storage for Web Applications”
### Diving In
- Persistant local storage is one of the areas where native client applications have held an advantage over web applications.
- Cookies were invented early in the web's history, and indeed they can be used for persistant local storage of small amounts of data, but they have three potientally dealbreaking downsides:
  - Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over.
  - Cookies aare included with every HTTP request, thereby sending data uncrpyed over the internet (unless your entire web application is served over SSL)
  - Cookies are limited to about 4 Kb of data - enough to slow down your application (see above), but not enought to be terribly useful.
- What we really want is
  - A lot of storage space on the client that persists beyond a page refresh and isn't transmitted to the server
### Intro
- The lastest version of pretty much every browser supports HTML5 storage... even Internet Explorer
- From your JS code, you'll access HTML5 Storage through the localStorage object on the global window. Before you can use it, you should *detect whether the browser supports it*. 
```javascript
function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
Instead of writing this function yourself, you can use Modernizr to detect support for HTML5 Storage.

if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
```
### Using HTML5 Storage
- HTML5 storage is based on named key/values pairs. 
- You store data based on a named key, then you can retrieve that data with the same key. 
- The named key is a string.
- The data can be any type supported by JS, including strings, booleans, integers, or floats. However the data is actually stored as a string.
- If you are storing and retrieving anything other than strings, you wiwl need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JS datatype.
```javascript
interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};
```
- Calling setItem() with a named key that already exists will silently overwrite the previous values. Calling getItem() with a non-existent key will return null rather than throw an exception.
- Like other JS objects, you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets. For example:
```javascript
var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
//…could be rewritten to use square bracket syntax instead:

var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;
//There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};

// Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

interface Storage {
  readonly attribute unsigned long length;
  getter DOMString key(in unsigned long index);
};
```
### Tracking Changes To The HTML5 Storage Area
- If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whwenver setItem(), removeItem(), or clear() is called and actually changes something.

### STORAGEEVENT OBJECT
- PROPERTY	TYPE	DESCRIPTION
- key	    string	the named key that was added, removed, or modified
- oldValue	   any	the previous value (now overwritten), or null if a new item was added
newValue	   any the new value, or null if an item was removed
url*	string	    the page which called a method that triggered this change
* Note: the url property was originally called uri. Some browsers shipped with that property before the specification changed. For maximum compatibility, you should check whether the url property exists, and if not, check for the uri property instead.