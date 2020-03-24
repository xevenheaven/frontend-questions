# JavaScript Questions

## Explain what is closure.
A JavaScript closure is when an inner function has access to its outer enclosing function's variables and properties.

## Explain what is IIFE.
An IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined.
```js
(function () {
    statements
})();
```

## Explain what is hoisting.
Every variable or function declaration brought to the top of its current scope.

## What is the function of delete operator?
The `delete` keyword is used to delete the property of an object, as well as its value.

## What is the difference between attributes and properties?
Attributes provide more details on an element e.g. id, type, value etc.
Properties are the values assigned to the property e.g. `type=”text”` etc.

## What are the ways to define a variable in JavaScript?
Three ways: `var`, `const`, `let`.

| var | let | const |
| --- | --- | ----- |
| globally scoped or function scoped | block scoped | block scoped |
| can be updated and re-declared within its scope | can be updated but not re-declared | can neither be updated nor re-declared |
| initialized with undefined | not initialised | not initialised |
| can be declared without being initialised | can be declared without being initialised | must be initialized during declaration |

## What is the difference between local storage and session storage?
The data stored in local storage is not sent back to the server for every HTTP request,
reducing the amount of traffic between client and server. It will stay until it is manually cleared.
While data stored in local storage has no expiration time, data stored in session storage
gets cleared when the page session ends, i.e. session storage will clear when the browser is closed.

## What is the difference between undefined and null?
Undefined means a variable has been declared but has not yet been assigned a value.
On the other hand, null is an assignment value. It can be assigned to a variable as a representation of no value.
Also, undefined and null are two distinct types: undefined is a type itself (undefined) while null is an object.

## What is an event bubbling in JavaScript?
Event bubbling is a way of event propagation in the HTML DOM API when an event occurs
in an element inside another element, and both elements have registered a handle for that event.
With bubbling, the event is first captured and handled by the innermost element
and then propagated to outer elements. The execution starts from that event and goes to its parent element.
Then the execution passes to its parent element and so on till the body element.
