
# JavaScript Functions – Simplified Notes

### Table of Contents
- [What is a Function?](#what-is-a-function)
- [Function Declaration](#function-declaration)
- [Function Invocation (Calling a Function)](#function-invocation-calling-a-function)
- [Function Parameters vs Arguments](#function-parameters-vs-arguments)
- [Function Expression](#function-expression)
- [Anonymous Function](#anonymous-function)
- [Return Statement](#return-statement)
- [Immediately Invoked Function Expression (IIFE)](#immediately-invoked-function-expression-iife)
- [Common Interview Questions](#common-interview-questions)

---

### What is a Function?
A **function** is a reusable block of code that performs a task. It helps you organize code, reuse it, and keep things simple.

Example:
```js
function greet() {
  console.log("Hello, Welcome!");
}
```

---

### Function Declaration
A **function declaration** defines a function using the `function` keyword.

Example:
```js
function sum(a, b) {
  return a + b;
}
```

> **Key Point:** The function is defined, but doesn't run until it's called.

---

### Function Invocation (Calling a Function)
After declaring a function, you **call** it by using its name followed by parentheses `()`.

Example:
```js
sum(5, 10); // Output: 15
```

> **Remember**: Calling a function runs the code inside it.

---

### Function Parameters vs Arguments
- **Parameters** are placeholders for values inside the function.
- **Arguments** are actual values you pass when calling the function.

Example:
```js
function greet(name) {  // `name` is a parameter
  console.log("Hello " + name);
}

greet("Vinod"); // "Vinod" is an argument
```

---

### Function Expression
A **function expression** stores a function in a variable. It can be **named** or **anonymous**.

Example (Anonymous):
```js
const sum = function(a, b) {
  return a + b;
};

console.log(sum(5, 10)); // Output: 15
```

> **Tip**: Function expressions aren’t hoisted, meaning they can’t be called before they’re defined.

---

### Anonymous Function
An **anonymous function** has no name. It’s often used when the function is assigned to a variable or passed as an argument.

Example:
```js
const result = function(a, b) {
  return a + b;
};

console.log(result(10, 15)); // Output: 25
```

---

### Return Statement
The **return** statement stops the function and sends a value back to where the function was called.

Example:
```js
function sum(a, b) {
  return a + b;
}

console.log(sum(5, 5)); // Output: 10
```

> **Important**: Code after `return` inside the function won’t run.

---

### Immediately Invoked Function Expression (IIFE)
An **IIFE** is a function that runs right after it’s created. It’s used to create a private scope.

Example:
```js
(function() {
  console.log("IIFE runs immediately!");
})();
```

Example with parameters:
```js
const result = (function(a, b) {
  return a + b;
})(5, 10);

console.log(result); // Output: 15
```

---

### Common Interview Questions

#### Calculator Function
Write a function that takes two numbers and an operator (`+`, `-`, `*`, `/`) and returns the result.

```js
const calculator = (num1, num2, operator) => {
  switch (operator) {
    case '+':
      return num1 + num2;
    case '-':
      return num1 - num2;
    case '*':
      return num1 * num2;
    case '/':
      return num2 === 0 ? 'Cannot divide by zero' : num1 / num2;
    default:
      return 'Invalid operator';
  }
};

console.log(calculator(5, 2, '+')); // Output: 7
```

---

#### String Reversal
Write a function to reverse a string **without using built-in methods**.

```js
const reverseString = (str) => {
  let reversed = '';
  for (let i = str.length - 1; i >= 0; i--) {
    reversed += str[i];
  }
  return reversed;
};

console.log(reverseString("JavaScript")); // Output: tpircSavaJ
```

---

#### Palindrome Check
Create a function to check if a string is a palindrome (reads the same backward as forward).

```js
const isPalindrome = (str) => {
  let reversed = '';
  for (let i = str.length - 1; i >= 0; i--) {
    reversed += str[i];
  }
  return str === reversed;
};

console.log(isPalindrome("level")); // Output: true
console.log(isPalindrome("javascript")); // Output: false
```

---

### Additional Tips and Notes:
- **Arrow Functions**: A shorter way to write functions.
  ```js
  const add = (a, b) => a + b;
  ```

- **Function Hoisting**: You can call a function **before** it’s declared, but this only works with function declarations, not function expressions.

- **Default Parameters**: You can give default values to function parameters.
  ```js
  function greet(name = "Guest") {
    console.log("Hello " + name);
  }
  greet(); // Output: Hello Guest
  ```

---

These notes simplify all the key concepts about JavaScript functions, making them easy to understand and **perfect for interview preparation**.
