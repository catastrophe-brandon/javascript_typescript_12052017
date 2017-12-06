# All About `this`

This inside a function `this` refers to the global object if the function is declared in the global scope.

Strange behavior when it comes to `this` related to the global scope.

If you add `'use strict';` the value of `this` is undefined when used inside a function on the global scope.
It also changes the value of this from a function inside a function in global scope.

Value of `this` is determined by how the function is invoked at runtime. This is because of prototype inheritance.
`this` points to the object that invoked the function.

`bind` produces a new function whose value of `this` will always be the object supplied as the argument.

`call` allows you to invoke a function and explicitly set the value of `this`.






