# JavaScript: Data Types

## Introduction
Data types define the type of values that a variable can hold in JavaScript. 

- Understanding data types is fundamental for writing robust, efficient, and error-free code.

---

In JavaScript, there are two main categories of data types:
1. **Primitive Types**
2. **Non-Primitive Types (Reference Types)**

## 1. Primitive Types
Primitive data types are basic and immutable (cannot be changed). There are 7 primitive types in JavaScript:

### a. `String`
- Used to represent text.
- Written inside quotes (`' '`, `" "`, or backticks `` ` ` `).
  
  **Example**:
  ```javascript
  let name = "John";

### b. Number

- Represents both integer and floating-point numbers.

- Can also be Infinity, -Infinity, and NaN (Not a Number).

  **Example**:
  ```javascript
  let age = 25;
  let price = 99.99;


### c. Boolean

- Represents true or false values.

  **Example**:
  ```javascript
  let isLoggedIn = true;


### d. Undefined

- A variable that has been declared but has not been assigned a value is undefined.

  **Example**:
  ```javascript
  let address;
  console.log(address); // undefined


### e. Null

- Represents an intentional absence of any object value.

  **Example**:
  ```javascript
  let emptyValue = null;


### f. Symbol

- Introduced in ES6, Symbol is a unique and immutable value, often used as object keys.

  **Example**:
  ```javascript
  let uniqueID = Symbol("id");


### g. BigInt

- Used to represent integers larger than the Number type can handle.

  **Example**:
  ```javascript
  let bigNumber =     123456789012345678901234567890n;


## 2. Non-Primitive Types (Reference Types)

These types store references to objects in memory.

### a. Object

- Used to store collections of data in key-value pairs.

  **Example**:
  ```javascript 
  let person = {
  name: "John",
  age: 30
};


### b. Array

- A special type of object used to store ordered lists of values.

  **Example**:
  ```javascript
  let numbers = [1, 2, 3, 4, 5];


### c. Function

- Functions are also objects in JavaScript and can be assigned to variables, passed as arguments, or returned by other functions.

  **Example**:
  ```javascript
  function greet() {
  console.log("Hello!");
}


### **Summary**

- Primitive Types: String, Number, Boolean, Undefined, Null, Symbol, BigInt

- Non-Primitive Types: Object, Array, Function


---

## Key Interview Questions

### 1. What is the difference between `null` and `undefined` in JavaScript?
- **null**: Represents an intentional absence of value.
- **undefined**: A variable is declared but not initialized.

```javascript
let a = null;
let b;
console.log(a); // null
console.log(b); // undefined
```

**Short Definition**: 
- `null` is intentionally assigned.
- `undefined` is automatically assigned by JavaScript.

---

### 2. What is the purpose of the `typeof` operator?
The `typeof` operator is used to determine the type of a variable.

```javascript
var myName = 1;
console.log(typeof myName); // Outputs: "number"
```

---

### 3. What is the result of `typeof null`?
The result of `typeof null` is `"object"`, which is a well-known bug in JavaScript.
```javascript
console.log(typeof null); // Outputs: "object"
```

---

### 4. How to convert a string to a number?
There are several ways to convert a string to a number:
1. Use the `+` operator.
2. Use the `Number()` function.

```javascript
let str = "10";
console.log(+str); // Outputs: 10
console.log(Number(str)); // Outputs: 10
```

---

### 5. How to convert a number to a string?
To convert a number to a string, you can:
1. Use the `.toString()` method.
2. Use template literals.

```javascript
let num = 5;
console.log(num.toString()); // Outputs: "5"
```

---

### 6. Explain Truthy and Falsy values.
In JavaScript, a value is either **truthy** or **falsy** in a boolean context.

- **Truthy Values**: Non-empty strings, non-zero numbers, objects, arrays.
- **Falsy Values**: `false`, `0`, `''`, `null`, `undefined`, `NaN`.

```javascript
let value = 0;
if (value) {
  console.log("Truthy");
} else {
  console.log("Falsy"); // This will run
}
```

---

### 7. What is the purpose of `parseInt()` and `parseFloat()`?

- **`parseInt()`** converts a string into an integer, ignoring any decimal part.
- **`parseFloat()`** converts a string into a floating-point number.

```javascript
let strInt = "42.5";
console.log(parseInt(strInt)); // Outputs: 42
console.log(parseFloat(strInt)); // Outputs: 42.5
```

**Key Differences**: `parseInt()` drops the decimal, while `parseFloat()` retains it.

---

### 8. What is `NaN` and why does `NaN === NaN` return false?
- **NaN** stands for "Not a Number" and is returned when a mathematical operation fails.
- **NaN** is not equal to anything, including itself.

```javascript
console.log(NaN === NaN); // Outputs: false
```

Use `isNaN()` to check if a value is NaN.

```javascript
console.log(isNaN("vinod")); // true
```

---

### 9. How do you check if a value is null, undefined, or NaN?
- **`null`**: `value === null`
- **`undefined`**: `typeof value === "undefined"`
- **`NaN`**: `isNaN(value)`

```javascript
let x = NaN;
console.log(isNaN(x)); // Outputs: true
```

---

## Bonus Concepts

### Strict Equality (`===`) vs Loose Equality (`==`)
- **Strict equality (`===`)** checks for both value and type.
- **Loose equality (`==`)** converts the values to the same type before comparing.

```javascript
console.log(5 == "5");  // true (loose equality)
console.log(5 === "5"); // false (strict equality)
```

---

### Type Coercion
JavaScript automatically converts values from one type to another during comparisons and operations.

```javascript
console.log("5" - 2); // Outputs: 3 (string converted to number)
```

---

### Template Literals
Template literals, introduced in ES6, allow easier string interpolation and multiline strings.

```javascript
let name = "John";
let greeting = `Hello, ${name}!`; 
console.log(greeting); // Outputs: "Hello, John!"
```

---

### Symbols for Unique Identifiers
Symbols are often used to create unique object keys.

```javascript
let symbol1 = Symbol('key');
let symbol2 = Symbol('key');
console.log(symbol1 === symbol2); // Outputs: false (symbols are always unique)
```

---

### Object.is()
`Object.is()` compares two values for strict equality, similar to `===` but with some key differences, such as correctly handling `NaN` and distinguishing `+0` from `-0`.

```javascript
console.log(Object.is(NaN, NaN)); // true
console.log(Object.is(+0, -0));   // false
```

---

## Conclusion
JavaScript's data types are foundational to programming in the language. Understanding how to use them properly can help prevent bugs, improve code clarity, and make coding more efficient. Mastering type coercion, strict vs loose equality, and the behavior of special values like `NaN` and `undefined` will make you a stronger JavaScript developer.
```


