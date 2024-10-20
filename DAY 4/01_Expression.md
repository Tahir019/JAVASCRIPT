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

## **Latest Concepts**

- **Type Coercion**: JavaScript automatically converts types when performing operations. Be cautious of unexpected results, especially with equality comparisons.

- **Short-circuit Evaluation**: Logical operators can skip evaluations. For example, in `true && anything`, `anything` won't be evaluated because the first operand is true.

---

This concludes your comprehensive notes on **Expressions and Operators** in JavaScript. Mastering these concepts is crucial for effective coding and performing well in interviews.
```
