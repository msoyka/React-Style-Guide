# Basic Javascript ES6 Principles

[Object Destructuring]((https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment))
---------------
> Object destructuring, or assignment destructuring, unpacks values from arrays, or properties from objects, into distinct variables.

```jsx 
const apple = {color: 'red', size: 'small'};
const {color, size} = apple;

console.log(color); // red
```

---

[Arrow Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
---------------
> An arrow function expression is a syntactically compact alternative to a regular function expression and works well with React components becuase is creates its own bindings to `this`, which previously had to be done manually.

```jsx 
const functionName = (param1, param2, …, paramN) => statements; 
```

---

[Const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) / [Let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) Variable Declarations
---------------
> - Introduce block level scoping in our code.
> - Remove variable hoisting.
> - Const is used for values that don't change
> - Let is used for values that do change

```jsx
const number = 42;

try {
  number = 99;
} catch(err) {
  console.log(err);
  // expected output: TypeError: invalid assignment to const `number'
  // Note - error messages will vary depending on browser
}

console.log(number);
// expected output: 42
```

```jsx
let x = 1;

if (x === 1) {
  let x = 2;

  console.log(x);
  // expected output: 2
}

console.log(x);
// expected output: 1
```

---

[Spread Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)
---------------
Spread syntax allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected.

```jsx
// Without spread operator
let mid = [3, 4];
let arr = [1, 2, mid, 5, 6];
console.log(arr); // [1, 2, [3, 4], 5, 6]

// With spread operator
let mid = [3, 4];
var arr = [1, 2, ...mid, 5, 6];
console.log(arr); // [1, 2, 3, 4, 5, 6]
```

---

[Array.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) Method
---------------
The map() method creates a new array with the results of calling a provided function on every element in the calling array. As it pertains to React, you can map through data array, and return a new array of React components or HTML elements wrapping the data. In addition, all React components that return multiple elements are wrapped in an array, so using the `.map()` method ties into React nicely.

```jsx
var colors = ["red", "green", "blue"];

// pass a function to map
const colorList = colors.map(color => `<li>${color}</li>`);

console.log(colorList);
// expected output: Array [<li>red</li>,<li>green</li>,<li>blue</li>]
```

---

[Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
---------------
Modules allow Javascript developers to separate pieces of code into new files, export that code, and then import them as a shared resource in another file. The increases the ease of following modular development principles natively within Javascript.

JavaScript has had modules for a long time. However, they were implemented via libraries, not built into the language. ES6 is the first time that JavaScript has built-in modules.


```jsx
// 📁 lib/shout.js
export const shout = (string) => `${string.toUpperCase()}!`;
```

```jsx
// 📁 index.js
import {shout} from './lib/shout.js';

const shoutHello = () => shout('Hello');
```