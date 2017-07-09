# DOMiNODE

A lightweight JavaScript library for DOM traversal and manipulation inspired by jQuery

[Demo](https://github.com/amandachen13/Snake)

## API

#### `DOMNodeCollection`

* a class that receives and stores an array of `HTMLElement`s
* prototype methods will be applied to every node in the array

#### `$l`

* the core function that receives either a `string` (expected to be a CSS selector that can identify nodes in the page) or an `instanceof` `HTMLElement`
* returns an instance of DOMNodeCollection

### DOM Traversal

#### `DOMNodeCollection.prototype.each(callback)`

* executes a callback for each node

#### `DOMNodeCollection.prototype.children()`

* returns a `DOMNodeCollection` of all children of each node

#### `DOMNodeCollection.prototype.parent()`

* returns a `DOMNodeCollection` of the parents of each node

#### `DOMNodeCollection.prototype.find(selector)`

* returns a `DOMNodeCollection` of all descendants of the nodes that match the selector

### DOM Manipulation

#### `DOMNodeCollection.prototype.html(innerHTML)`

* updates the `innerHTML` of each node if an argument is provided
* returns the `innerHTML` of the first node if an argument is not provided

#### `DOMNodeCollection.prototype.empty()`

* clears out the content of each node

#### `DOMNodeCollection.prototype.append(el)`

* accepts either a `DOMNodeCollection`, an `HTMLelement`, or a `string`
* appends the `outerHTML` of each element in the argument to the `innerHTML` of each node

#### `DOMNodeCollection.prototype.remove()`

* removes the HTML of each node from the DOM

#### `DOMNodeCollection.prototype.attr(name, value)`

* gets the value of an attribute for the first node if an attribute name is provided
* sets the value of an attribute for each node if an attribute name and a value are provided

#### `DOMNodeCollection.prototype.addClass(class)`

* adds a class to each node

#### `DOMNodeCollection.prototype.removeClass(class)`

* removes a class from each node

### Event Handling

#### `DOMNodeCollection.prototype.on(eventType, callback)`

* attaches event handler on each node

#### `DOMNodeCollection.prototype.off(eventType)`

* removes event handler from each node

### AJAX

#### `$l.ajax(options)`

* receives an options object or uses defaults object
* makes an HTTP request and delivers the proper response to the success/error callback

#### `$l.extend(defaultObj, ...objects)`

* merges the contents of two or more objects together into the first object
