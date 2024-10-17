# JavaScript: Data Types

## Introduction
Data types define the type of values that a variable can hold.

---

## Primitive Data Types
### 1. Number
Represents numeric values, including integers and floating-point numbers.
```javascript
var myFavNum = -5;
console.log(myFavNum);
```

### 2. String
Represents a sequence of characters enclosed in single or double quotes.
```javascript
var myName = 'vinod';
console.log(myName);
```

### 3. Boolean
Represents a logical entity with two values: `true` or `false`.
```javascript
var isRaining = false;
var areYouAwesome = true;
console.log(isRaining);
```

### 4. Undefined
Represents the absence of a value or an uninitialized variable.
```javascript
var vinod;
console.log(vinod);
```

### 5. Null
Represents the absence of a value. It is often used to explicitly indicate that a variable or object property has no assigned value.
```javascript
var badMemories = null;
console.log(badMemories);
```

### 6. BigInt
Represents integers of arbitrary precision (available since ECMAScript 2020).
```javascript
const bigNumber = 1234567890123456789012345678901234567890n;
```

### 7. Symbol
Represents a unique and immutable data type, often used to create unique identifiers.
```javascript
const mySymbol = Symbol("description");
```

---

## Data Types Interview Questions

### 1. What is the difference between null and undefined in JavaScript?
- **null**: Imagine an empty box. The box exists, but there's nothing valuable inside it.
  - Example: A toy box that is null means there are no toys inside; the box is not broken; it just doesn’t have anything interesting in it right now.
  
- **undefined**: Imagine a box that wasn't opened yet. You know the box is there, but you haven't put anything inside or checked what's in it.
  - Example: A gift box that is undefined means you haven't opened it yet. Right now, it's undefined because you haven't checked or filled it with anything yet.

**Summary**: Null is like having an empty box on purpose, and undefined is like having a box you haven't opened yet.

---

### 2. What is the purpose of the `typeof` operator in JavaScript?
```javascript
var myName = 1;
console.log(myName); // Outputs: 1
console.log(typeof myName); // Outputs: "number"
```

### 3. What is the result of `typeof null` in JavaScript?
```javascript
var badMemories = null;
console.log(badMemories); // Outputs: null
console.log(typeof null); // Outputs: "object"
```

### 4. What are primitive data types in JavaScript?
- Number
- String
- Boolean
- Undefined
- Null
- BigInt
- Symbol

### 5. How to convert a string to a number?
Add the `+` sign before the string.
```javascript
var myFavNum = "10";
console.log(typeof +myFavNum); // Outputs: "number"
console.log(typeof Number(myFavNum)); // Outputs: "number"
```

### 6. How to convert a number to a string?
Add an empty string after the number.
```javascript
var str = 5;
console.log(typeof str.toString()); // Outputs: "string"
```

### 7. Explain the concept of truthy and falsy values in JavaScript. Provide examples.
- **Truthy values** are treated as true when used in conditions:
  - `true`
  - Any non-empty string (e.g., "hello")
  - Any non-zero number (e.g., 42)
  - Arrays and objects, even if they're empty

- **Falsy values** are treated as false in boolean contexts:
  - `false`
  - `0` (zero)
  - `''` (an empty string)
  - `null`
  - `undefined`
  - `NaN` (Not a Number)

### 8. To check if a non-empty string is truthy or falsy in JavaScript:
```javascript
var myName = -5;
if (myName) {
  console.log("This is a truthy value.");
} else {
  console.log("It's a falsy value.");
}
```

---

## Bonus: parseInt & parseFloat Section

### parseInt
**Definition**: `parseInt` is used to parse a string and convert it to an integer (whole number).
```javascript
const myString = "42";
const myNumber = parseInt(myString);
console.log(myNumber); // Output: 42

const myStringFloat = "42.5";
const myNumberFloat = parseInt(myStringFloat);
console.log(myNumberFloat); // Output: 42
```

### parseFloat
**Definition**: `parseFloat` is used to parse a string and convert it to a floating-point number (decimal number).
```javascript
const myString = "42.5";
const myNumber = parseFloat(myString);
console.log(myNumber); // Output: 42.5
```

### Key Differences
- `parseInt` is used for converting to integers and ignores anything after the decimal point.
- `parseFloat` is used for converting to floating-point numbers, preserving the decimal part.
- Both functions will attempt to convert as much of the string as possible until an invalid character is encountered.

### More Examples
```javascript
console.log(parseInt("123")); // 123 (default base-10)
console.log(parseInt("123", 10)); // 123 (explicitly specify base-10)
console.log(parseInt("   123 ")); // 123 (whitespace is ignored)
console.log(parseInt("077")); // 77 (leading zeros are ignored)
console.log(parseInt("1.9")); // 1 (decimal part is truncated)
console.log(parseFloat("1.9")); // 1.9
```

### When There Will Not Be an Output
```javascript
console.log(parseInt("&123")); // NaN (input can't be converted to an integer)
console.log(parseInt("-123")); // -123
console.log(parseInt("xyz")); // NaN (input can't be converted to an integer)
```

### What is the purpose of the NaN value in JavaScript?
`NaN` stands for "Not a Number" and is returned when a mathematical operation doesn't yield a valid number. To check whether a value is a number or not, you can use the `isNaN()` function.
```javascript
console.log(isNaN("vinod")); // true
console.log(parseInt("xyz")); // NaN
console.log(parseInt("@#$")); // NaN
```

### NaN === NaN, Why is it false?
```javascript
if (NaN == NaN) {
  console.log("Both are equal.");
} else {
  console.log("Not equal."); // This will execute
}
```

---

```
