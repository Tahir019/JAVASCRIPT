# JavaScript Interview Notes

## 1. Introduction to JavaScript
JavaScript is a lightweight, interpreted programming language used to build dynamic web content like interactive forms, animations, and more.

---

## 2. Variables
### What are Variables?
Variables store data values that can be used and modified in your program.

### Declaring Variables:
- **`var`**: Function-scoped. Can be updated and re-declared.
- **`let`**: Block-scoped. Can be updated but not re-declared.
- **`const`**: Block-scoped. Cannot be updated or re-declared.

```javascript
var x = 5;
let y = 10;
const z = 15;
```

---

## 3. Data Types
JavaScript has two types of data:

### Primitive Types:
- **Number**: Represents both integer and floating-point numbers.
  ```javascript
  let age = 25;
  ```
- **String**: A sequence of characters enclosed in quotes.
  ```javascript
  let name = "Tahir";
  ```
- **Boolean**: Represents one of two values: `true` or `false`.
  ```javascript
  let isStudent = true;
  ```
- **Undefined**: A variable that has been declared but not assigned a value.
- **Null**: Represents an intentional absence of any object value.
- **Symbol**: A unique and immutable value used as an object property key.
- **BigInt**: Used to represent integers with arbitrary precision.

### Non-Primitive Types:
- **Object**: A collection of key-value pairs.
- **Array**: A special type of object used to store ordered lists of values.

---

## 4. Operators
### Arithmetic Operators:
Used for basic math operations: `+`, `-`, `*`, `/`, `%`.

```javascript
let sum = 5 + 3; // 8
```

### Comparison Operators:
Used to compare values: `==`, `===`, `!=`, `!==`, `>`, `<`.

```javascript
5 == "5";  // true
5 === "5"; // false
```

### Logical Operators:
Used for combining conditions: `&&` (and), `||` (or), `!` (not).

```javascript
if (age > 18 && isStudent) {
  console.log("You are an adult student.");
}
```

---

## 5. Functions
### What is a Function?
A function is a block of code designed to perform a particular task, which can be reused.

### Function Example:
```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
console.log(greet("Tahir")); // "Hello, Tahir!"
```

### Arrow Function:
```javascript
const greet = (name) => `Hello, ${name}!`;
```

---

## 6. Control Flow
### If-Else Statement:
```javascript
if (age >= 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}
```

### Switch Case:
```javascript
switch (day) {
  case 1:
    console.log("Monday");
    break;
  case 2:
    console.log("Tuesday");
    break;
  default:
    console.log("Other day");
}
```

### Loops:
#### For Loop:
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i); // 0, 1, 2, 3, 4
}
```

#### While Loop:
```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

---

## 7. Objects
Objects are collections of key-value pairs.

```javascript
let person = {
  name: "Tahir",
  age: 25,
  greet() {
    console.log("Hello!");
  }
};
console.log(person.name); // "Tahir"
person.greet(); // "Hello!"
```

---

## 8. Arrays
Arrays store multiple values in a single variable.

```javascript
let colors = ["red", "green", "blue"];
console.log(colors[0]); // "red"
```

### Common Array Methods:
- **`push()`**: Adds an item to the end of the array.
- **`pop()`**: Removes the last item.
- **`length`**: Returns the number of items in the array.

---

## 9. Events
Events are actions that happen in the browser (like clicks).

### Event Handling Example:
```javascript
document.getElementById("myButton").addEventListener("click", function() {
  alert("Button clicked!");
});
```

---

## 10. DOM Manipulation
The **Document Object Model (DOM)** represents the page structure as objects that can be modified using JavaScript.

```javascript
document.getElementById("demo").innerHTML = "Hello World!";
```

---

## 11. Promises
A promise is used to handle asynchronous operations (like data fetching).

### Promise Example:
```javascript
let myPromise = new Promise(function(resolve, reject) {
  // some async work
  resolve("Success!");
});

myPromise.then(function(result) {
  console.log(result); // "Success!"
});
```

---

## 12. ES6+ Features
### Arrow Functions:
Shorter syntax for functions.
```javascript
const sum = (a, b) => a + b;
```

### Template Literals:
Allows embedding variables into strings.
```javascript
let name = "Tahir";
console.log(`Hello, ${name}!`);
```

### Destructuring:
Extract values from objects or arrays.
```javascript
let [a, b] = [1, 2];
let {name, age} = person;
```

---

## 13. Hoisting
**Hoisting** refers to JavaScript moving declarations to the top of their scope before execution.

```javascript
console.log(x); // undefined
var x = 5;
```

---

## 14. Closures
A **closure** is a function that has access to its outer scope even after the outer function has returned.

```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    return count;
  };
}

const counter = outer();
console.log(counter()); // 1
console.log(counter()); // 2
```
```

