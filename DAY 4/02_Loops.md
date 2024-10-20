# JavaScript Conditional Statements & Loops

## Table of Contents
- [Conditional Statements](#conditional-statements)
  - [If Statement](#if-statement)
  - [If...Else Statement](#if-else-statement)
  - [Else If Ladder](#else-if-ladder)
  - [Switch Statement](#switch-statement)
  - [Ternary Operator](#ternary-operator)
  - [Advanced Conditional Techniques](#advanced-conditional-techniques)
- [Loops](#loops)
  - [For Loop](#for-loop)
  - [While Loop](#while-loop)
  - [Do...While Loop](#do-while-loop)
- [Interview Questions](#interview-questions)
  - [Conditional Questions](#conditional-questions)
  - [Loop Questions](#loop-questions)
- [Unique Concepts and Best Practices](#unique-concepts-and-best-practices)
- [Homework](#homework)

---

## Conditional Statements

### If Statement
The `if` statement executes a block of code only if a specified condition is `true`.

#### Syntax:
```javascript
if (condition) {
  // Code to execute if condition is true
}
```

#### Example:
```javascript
let temperature = 20;
if (temperature > 25) {
  console.log("It's warm outside!");
}
```

#### Key Points:
- The condition is evaluated; if it's true, the code runs.
- If the condition is false, the block is skipped.

---

### If...Else Statement
The `if...else` statement runs a block of code if the condition is `true`; otherwise, it runs another block of code.

#### Syntax:
```javascript
if (condition) {
  // Code to execute if true
} else {
  // Code to execute if false
}
```

#### Example:
```javascript
let temperature = 18;
if (temperature > 25) {
  console.log("It's hot outside");
} else {
  console.log("It's a bit chilly");
}
```

---

### Else If Ladder
The `else if` ladder is useful when you need to test multiple conditions sequentially.

#### Syntax:
```javascript
if (condition1) {
  // Code if condition1 is true
} else if (condition2) {
  // Code if condition2 is true
} else {
  // Code if none of the above are true
}
```

#### Example:
```javascript
let time = 12;
if (time < 12) {
  console.log("Good morning");
} else if (time < 18) {
  console.log("Good afternoon");
} else {
  console.log("Good evening");
}
```

---

### Switch Statement
The `switch` statement is used to compare a value against multiple possible cases.

#### Syntax:
```javascript
switch (expression) {
  case value1:
    // Code if expression === value1
    break;
  case value2:
    // Code if expression === value2
    break;
  default:
    // Code if no cases match
}
```

#### Example:
```javascript
let day = "Tuesday";
switch (day) {
  case "Monday":
    console.log("Start of the week");
    break;
  case "Tuesday":
    console.log("It's Tuesday");
    break;
  default:
    console.log("Invalid day");
}
```

#### Key Points:
- Always include a `break` statement to prevent fall-through.
- The `default` case is optional and runs if no cases match.

---

### Ternary Operator
A shorthand for `if...else`, the ternary operator is used for simple conditions.

#### Syntax:
```javascript
condition ? expr1 : expr2;
```

#### Example:
```javascript
let age = 20;
let canVote = (age >= 18) ? "Yes, you can vote" : "No, you cannot vote";
console.log(canVote);
```

#### Key Points:
- Best for short, simple condition checks.
- Avoid using for complex logic as it can make code harder to read.

---

### Advanced Conditional Techniques
- **Optional Chaining (`?.`)**: Used in conditional checks to avoid errors when trying to access properties of `null` or `undefined` objects.

#### Example:
```javascript
let user = { name: "Alice" };
console.log(user?.profile?.age); // undefined
```

---

## Loops

### For Loop
A `for` loop repeats code for a specific number of iterations.

#### Syntax:
```javascript
for (initialization; condition; increment) {
  // Code to execute
}
```

#### Example:
```javascript
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

#### Key Points:
- Initialization runs once at the beginning.
- The condition is checked before every iteration.
- The increment runs after each iteration.

---

### While Loop
The `while` loop runs as long as the condition remains `true`.

#### Syntax:
```javascript
while (condition) {
  // Code to execute
}
```

#### Example:
```javascript
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}
```

#### Key Points:
- Check the condition before running the code.
- Beware of infinite loops if the condition never becomes `false`.

---

### Do...While Loop
The `do...while` loop runs the code block at least once, then checks the condition.

#### Syntax:
```javascript
do {
  // Code to execute
} while (condition);
```

#### Example:
```javascript
let i = 1;
do {
  console.log(i);
  i++;
} while (i <= 5);
```

---

## Interview Questions

### Conditional Questions
1. **What is the difference between `if...else` and `switch`?**  
   - `if...else` can handle ranges and complex conditions, whereas `switch` is more suitable for comparing a single expression to multiple values.
   
2. **What is the ternary operator?**  
   - It's a shorthand for `if...else`, useful for short, simple conditions.

---

### Loop Questions
1. **Explain the difference between a `for` loop and a `while` loop.**  
   - A `for` loop is best when you know the number of iterations beforehand. A `while` loop is used when the number of iterations is unknown.

2. **What is an infinite loop? How can it occur?**  
   - An infinite loop occurs when the loop's condition never becomes `false`. This can happen if the condition or increment is not correctly implemented.

---

## Unique Concepts and Best Practices

### Loop Optimization Techniques
- **Loop Unrolling**: This optimization technique reduces the overhead of loop control by decreasing the number of iterations, while performing more work in each iteration.

### Memoization in Loops
- Store previously calculated results to avoid redundant calculations during loops.

---

## Homework
1. Write a JavaScript program that checks if a number is prime using a `for` loop.
2. Create a multiplication table for a user-defined number using a `while` loop.
3. Write a program that checks if a given year is a leap year using a `do...while` loop.
```