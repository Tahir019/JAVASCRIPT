# JavaScript: Values and Variables

## Introduction
In JavaScript, values and variables are fundamental concepts that form the basis of programming.

---

## Values
A **value** is a piece of information that a program can work with. It can be:
- A number
- Text (string)
- A boolean (`true`/`false`)
- More complex data types

---

## Variables
A **variable** is a container that holds a value. It has a name and can be used to store and manipulate data in a program.

### Example
```javascript
console.log("Welcome to the best JS course!");

var myAge = 30;
console.log(myAge);
```

---

## Variable Naming Rules
When creating variables, there are specific rules to follow:

### Valid Variable Names
```javascript
var my_firstName = "John"; // Valid: starts with a letter
// Explanation: This is a valid variable name. It starts with a letter, and the subsequent characters include letters, numbers, and an underscore.

var _myLastName$ = "Doe"; // Valid: starts with an underscore
// Explanation: This is a valid variable name. It starts with an underscore, and the subsequent characters include letters, numbers, and a dollar sign.

var $cityName = "New York"; // Valid: starts with a dollar sign
// Explanation: This is a valid variable name. It starts with a dollar sign, and the subsequent characters include letters. 
```

### Invalid Variable Names
```javascript
var 123myAge = 25; // Invalid: starts with a number
// Explanation: This is not a valid variable name. It starts with a number, which is not allowed as per JavaScript naming rules. Variable names cannot begin with a digit.

var my@Email = "john@example.com"; // Invalid: includes special character '@'
// Explanation: This is not a valid variable name. It includes the special character '@', which is not allowed in JavaScript variable names. Only letters, numbers, underscores, and dollar signs are allowed.
```
```
