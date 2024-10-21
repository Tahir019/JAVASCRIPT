# JavaScript Expressions and Operators

---

## **What are Expressions, Operands, and Operators?**

- **Expression**: A piece of code that produces a value.
- **Operand**: A value or variable that operators work on.
- **Operator**: A symbol that performs operations on operands.

---

## **Types of Operators in JavaScript**

1. **Assignment Operators**
2. **Arithmetic Operators**
3. **Comparison Operators**
4. **Logical Operators**
5. **String Operators**
6. **Conditional (Ternary) Operator**

---

### **1. Assignment Operators**

- **Definition**: Symbols used to assign values to variables.

  **Examples**:
  ```javascript
  var myFavNum = 15; // Assigns 15 to myFavNum
  var channelName = 'Thapa Technical';
  ```

---

### **2. Arithmetic Operators**

- **Definition**: Perform basic mathematical operations.

  - **Addition (+)**:
    ```javascript
    var x = 5, y = 10;
    console.log(x + y); // 15
    ```

  - **Subtraction (-)**:
    ```javascript
    var a = 10, b = 7;
    console.log(a - b); // 3
    ```

  - **Multiplication (*)**:
    ```javascript
    var p = 4, q = 6;
    console.log(p * q); // 24
    ```

  - **Division (/)**:
    ```javascript
    var m = 15, n = 3;
    console.log(m / n); // 5
    ```

  - **Modulus (%)**:
    ```javascript
    var c = 17, d = 5;
    console.log(c % d); // 2
    ```

  - **Challenge**: What will be the output of `var result = "hello" / 2;`?
  
---

### **3. Comparison Operators**

- **Definition**: Compare values and return a Boolean result.

  - **Equal (==)**:
    ```javascript
    console.log(5 == "5"); // true
    ```

  - **Strict Equal (===)**:
    ```javascript
    console.log(5 === "5"); // false
    ```

  - **Not Equal (!=)**:
    ```javascript
    console.log(5 != 5); // false
    ```

  - **Greater Than (>)**:
    ```javascript
    console.log(10 > 5); // true
    ```

  - **Less Than (<)**:
    ```javascript
    console.log(5 < 10); // true
    ```

  - **Greater Than or Equal To (>=)**:
    ```javascript
    console.log(10 >= 10); // true
    ```

  - **Less Than or Equal To (<=)**:
    ```javascript
    console.log(5 <= 10); // true
    ```

- **Interview Question**: What is the difference between `==` and `===`?

---

### **4. Logical Operators**

- **Definition**: Used to create complex conditions.

  - **Logical AND (&&)**:
    ```javascript
    var x = 5, y = 10;
    console.log(x > 0 && y < 0); // false
    ```

  - **Logical OR (||)**:
    ```javascript
    var a = 15, b = 0;
    console.log(a > 10 || b > 10); // true
    ```

  - **Logical NOT (!)**:
    ```javascript
    var isOpen = false;
    console.log(!isOpen); // true
    ```

- **Interview Question**: Write a program to determine if a person is eligible to drive based on age and license status.

---

### **5. String Operators**

- **Definition**: Used to concatenate strings.

  **Example**:
  ```javascript
  var str1 = "Hello", str2 = "World";
  console.log(str1 + " " + str2); // Hello World
  ```

- **Interview Question**: What will `console.log("5" + 3);` output? // Outputs "53"

---

### **6. Conditional (Ternary) Operator**

- **Definition**: A shorthand for `if...else`.

  **Syntax**:
  ```javascript
  condition ? expressionIfTrue : expressionIfFalse;
  ```

  **Example**:
  ```javascript
  var age = 19;
  var result = age >= 18 ? "Yes" : "No";
  console.log(result); // Yes
  ```

- **Interview Question**: Use a ternary operator to check if a student's score is a pass or fail.

---

### **7. Unary Operators**

- **Definition**: Operate on a single operand.

  - **Unary Plus (+)**:
    ```javascript
    console.log(+3); // 3
    ```

  - **Unary Negation (-)**:
    ```javascript
    console.log(-5); // -5
    ```

  - **Prefix Increment (++x)**:
    ```javascript
    var x = 5;
    console.log(++x); // 6
    ```

  - **Postfix Increment (x++)**:
    ```javascript
    var y = 5;
    console.log(y++); // 5
    console.log(y); // 6
    ```

---

## **Combined Interview Questions**

1. **What is the output of `console.log(typeof ("5" - 3));`?**
2. **What happens in `console.log(2 < 12 < 5);`?**
3. **What does `console.log("20" + 10 + 10);` output?**

---

# **Latest JavaScript Concepts**

### **1. Type Coercion**
- **Explanation**: 
  JavaScript automatically converts data from one type to another when performing operations. This is called type coercion.
  
  - It can convert strings to numbers, numbers to strings, and other types to fit the operation.
  - **Be cautious**: This can lead to unexpected results, especially when using the `==` equality operator, which allows type coercion.
  
  **Example**:
  ```js
  "5" + 3;    // "53" (String concatenation: "5" is a string, 3 becomes part of the string)
  "5" - 3;    // 2 (Type coercion: "5" is converted to a number for subtraction)

2. Short-circuit Evaluation

Explanation: JavaScript uses short-circuit evaluation with logical operators (&& and ||):

&& (AND): If the first operand is false, it won't evaluate the second operand because the overall result will always be false.

|| (OR): If the first operand is true, it skips evaluating the second operand because the overall result will be true.


Example:

true && console.log("This will print");  // This will print (both sides are evaluated)
false && console.log("This won't print");  // This won't print (skips the second evaluation)

true || console.log("This won't print");   // This won't print (first operand is true, so skips second)



---

Key Takeaway:

Type coercion can cause unexpected results; use === for strict comparisons to avoid this.

Short-circuit evaluation helps improve performance by skipping unnecessary evaluations.



# Answer Key

# JavaScript Interview Questions and Challenges

### **Challenge**: What will be the output of `var result = "hello" / 2;`?
- **Answer**: 
  The output will be `NaN` (Not-a-Number). In JavaScript, trying to perform arithmetic with a string that doesn't represent a number will result in `NaN`.

---

### **Interview Question**: What is the difference between `==` and `===`?
- **Answer**: 
  - `==` is the equality operator that compares values **after** converting their types if needed (type coercion).
  - `===` is the strict equality operator that compares both the **value** and the **type**. No type conversion happens.
  
  **Example**:
  ```js
  5 == "5";  // true (because "5" is converted to 5)
  5 === "5"; // false (different types: number and string)


---

Interview Question: Write a program to determine if a person is eligible to drive based on age and license status.

Answer:

function canDrive(age, hasLicense) {
  if (age >= 18 && hasLicense) {
    return "Eligible to drive";
  } else {
    return "Not eligible to drive";
  }
}

console.log(canDrive(20, true)); // Eligible to drive
console.log(canDrive(16, false)); // Not eligible to drive



---

Interview Question: What will console.log("5" + 3); output?

Answer: The output will be "53". This is because the + operator concatenates strings, so the number 3 is converted to a string and added to "5", resulting in "53".



---

Interview Question: Use a ternary operator to check if a student's score is a pass or fail.

Answer:

let score = 75;
let result = (score >= 50) ? "Pass" : "Fail";
console.log(result); // Pass



---

Combined Interview Questions

1. What is the output of console.log(typeof ("5" - 3));?

Answer: The output will be "number". Even though "5" is a string, the - operator forces a numeric conversion, so "5" - 3 becomes 5 - 3, which results in 2, and the type of 2 is "number".



---

2. What happens in console.log(2 < 12 < 5);?

Answer: The output will be true. Here's why:

First, 2 < 12 is true.

Then, true < 5 is evaluated. In JavaScript, true is converted to 1, and 1 < 5 is true.




---

3. What does console.log("20" + 10 + 10); output?

Answer: The output will be "201010". This happens because the first + concatenates the string "20" with 10, resulting in "2010". Then "2010" is concatenated with 10, resulting in "201010".



---


```
