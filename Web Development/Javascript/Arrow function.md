#javascript #javascript-fundamentals #programming_languages 

The arrow function in javascript provides for a shorten form of creating functions. This is done by using => to declare the function.

Example of this:
let myFunction = (a, b) => a * b;

The example above created an entire function in one line. This can be even simpler when considering this simple rules:

- The parentheses aren't need if you are only passing one parameter.
- No return method needs to be passed if only one statement is being provided.
- However when there is no parameters being passed into the function, make sure to have () in its place.

They are some differences between a regular function call and this one when it comes to handling the this keyword. If you would like to read more: https://www.w3schools.com/js/js_arrow_function.asp