# JavaScript Interview Preparation Notes

## 1. Expressions and Operators

### Definitions:
- **Expression**: A combination of values, variables, operators, and functions that evaluates to a value.
- **Operator**: A symbol that performs operations on operands. 
- **Operand**: A value on which an operator performs an operation.

### Types of Operators:
1. **Assignment Operators**: Assigns values to variables.
   - Example: `let x = 5;`

2. **Arithmetic Operators**: Performs mathematical operations.
   - `+` (Addition), `-` (Subtraction), `*` (Multiplication), `/` (Division), `%` (Modulus)
   - Example: `let sum = 5 + 10;`

3. **Comparison Operators**: Compares values.
   - `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
   - Example: `console.log(5 === '5'); // false`

4. **Logical Operators**: Combines boolean values.
   - `&&` (AND), `||` (OR), `!` (NOT)
   - Example: `console.log(true && false); // false`

5. **Unary Operators**: Operates on a single operand.
   - `+` (Unary Plus), `-` (Unary Negation), `++`, `--`
   - Example: `let x = 5; x++; // x is now 6`

6. **Ternary Operator**: A shorthand for `if-else`.
   - Syntax: `condition ? expr1 : expr2`
   - Example: `let status = (age >= 18) ? "Adult" : "Minor";`

### Important Interview Questions:
- **Q: What is the difference between `==` and `===`?**
  - `==` checks for equality with type coercion, while `===` checks for equality without type coercion.
  
- **Q: How do you concatenate strings in JavaScript?**
  - Use the `+` operator or template literals (`` `${variable}` ``).

---

## 2. Loops

### Definitions:
- **Loop**: A structure that repeats a block of code as long as a specified condition is true.

### Types of Loops:
1. **For Loop**: Executes a block of code a specific number of times.
   - Example:
     ```javascript
     for (let i = 0; i < 5; i++) {
       console.log(i);
     }
     ```

2. **While Loop**: Repeats as long as the condition is true.
   - Example:
     ```javascript
     let i = 0;
     while (i < 5) {
       console.log(i);
       i++;
     }
     ```

3. **Do...While Loop**: Executes code at least once, then repeats based on the condition.
   - Example:
     ```javascript
     let i = 0;
     do {
       console.log(i);
       i++;
     } while (i < 5);
     ```

### Important Interview Questions:
- **Q: What is the difference between a `for` loop and a `while` loop?**
  - A `for` loop is typically used when the number of iterations is known, while a `while` loop is used when the number of iterations is unknown.

- **Q: How can you prevent an infinite loop?**
  - Ensure the loop's condition will eventually evaluate to false and increment/decrement the loop variable appropriately.

---

## 3. Functions

### Definitions:
- **Function**: A reusable block of code that performs a specific task. It can take parameters and return a value.

### Function Types:
1. **Function Declaration**:
   - Syntax: 
     ```javascript
     function functionName(parameters) {
       // code to be executed
     }
     ```
   - Example:
     ```javascript
     function add(a, b) {
       return a + b;
     }
     ```

2. **Function Expression**: A function defined within an expression.
   - Example:
     ```javascript
     const multiply = function(a, b) {
       return a * b;
     };
     ```

3. **Arrow Function**: A concise syntax for writing functions.
   - Syntax:
     ```javascript
     const functionName = (parameters) => {
       // code
     };
     ```
   - Example:
     ```javascript
     const divide = (a, b) => a / b;
     ```

### Important Interview Questions:
- **Q: What is a closure in JavaScript?**
  - A closure is a function that retains access to its lexical scope, even when the function is executed outside that scope.

- **Q: How do you handle errors in JavaScript functions?**
  - Use `try...catch` blocks to catch and handle exceptions.
  
- **Q: What are higher-order functions?**
  - Functions that take other functions as arguments or return functions.

---

## 4. Hard Interview Questions
- **Q: Explain the concept of 'hoisting' in JavaScript.**
  - Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope before code execution. This applies to variables (using `var`) and function declarations.

- **Q: What is the output of the following code?**
  ```javascript
  console.log(typeof (null)); // ?
  ```
  - **Answer**: `object` (this is a known bug in JavaScript).

---

### Conclusion
This guide provides concise definitions, examples, and critical interview questions for Expressions and Operators, Loops, and Functions in JavaScript. Master these concepts to excel in your interviews!

```
