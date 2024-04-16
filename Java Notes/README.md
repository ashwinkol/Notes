# Java Basic Elements

# Data Types And Literals

In Java, data types represent the type of data that can be stored in variables. Here are the main data types in Java:

1. **Primitive Data Types**:
   - **byte**: 8-bit signed integer. Range: -128 to 127.
   - **short**: 16-bit signed integer. Range: -32,768 to 32,767.
   - **int**: 32-bit signed integer. Range: -2^31 to 2^31-1.
   - **long**: 64-bit signed integer. Range: -2^63 to 2^63-1.
   - **float**: 32-bit floating point. Represents fractional numbers.
   - **double**: 64-bit floating point. Represents fractional numbers with double precision.
   - **char**: 16-bit Unicode character. Represents a single character.
   - **boolean**: Represents true or false.


<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/DataTypeSize.png)](https://github.com/ashwinkol/Notes/tree/main/)

</div>


2. **Reference Data Types**:
   - **Class/Object**: Instances of classes created using the `new` keyword.
   - **Array**: A collection of elements of the same type, stored in a contiguous memory location.
   - **Interface**: Similar to classes but only contain abstract methods and constants.

These data types can be further categorized as:

- **Primitive Data Types**: byte, short, int, long, float, double, char, boolean.
- **Reference Data Types**: Class/Object, Array, Interface.


[![Java Data Types](/Java%20Notes/images/Data%20Types.jpg)](https://github.com/ashwinkol/Notes/tree/main/)

---

## Arithmetic Operators In Java

In Java, operators are symbols that perform operations on operands (variables, values, or expressions). Here are the main categories of operators in Java:

1. **Arithmetic Operators**:
   - Addition (`+`)
   - Subtraction (`-`)
   - Multiplication (`*`)
   - Division (`/`)
   - Modulus (`%`) - Returns the remainder of a division.

2. **Assignment Operators**:
   - Assignment (`=`)
   - Compound Assignment (e.g., `+=`, `-=`, `*=`, `/=`, `%=`)

3. **Comparison Operators**:
   - Equal to (`==`)
   - Not equal to (`!=`)
   - Greater than (`>`)
   - Less than (`<`)
   - Greater than or equal to (`>=`)
   - Less than or equal to (`<=`)

4. **Logical Operators**:
   - Logical AND (`&&`)
   - Logical OR (`||`)
   - Logical NOT (`!`)

5. **Bitwise Operators**:
   - Bitwise AND (`&`)
   - Bitwise OR (`|`)
   - Bitwise XOR (`^`)
   - Bitwise NOT (`~`)
   - Left Shift (`<<`)
   - Right Shift (`>>`)
   - Unsigned Right Shift (`>>>`)

6. **Unary Operators**:
   - Unary plus (`+`)
   - Unary minus (`-`)
   - Increment (`++`)
   - Decrement (`--`)
   - Logical NOT (`!`)
   - Bitwise NOT (`~`)
   - Type Cast (`(type)`)

7. **Conditional (Ternary) Operator**:
   - `(condition) ? (expression1) : (expression2)`

8. **Instanceof Operator**:
   - `instanceof`

---

# Type Casting In Java

- Implicit Casting (Widening)
  - BSC IF LD

  - Compiler is responsible to perform this typecasting

   - Whenever we assign smaller datatype value to the bigger data type variable implicit type casting will be performed.

  - This is also known as widening or upcasting.

  - There is no loss of information in this typecasting.

  
<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/ImplicitTypeCasting.jpg)](https://github.com/ashwinkol/Notes/tree/main/)

</div>



- Explicit Casting (Narrowing)
  - BSC IL FD

  - Programmer is responsible to perform this type of type casting


  - Whenever we assign bigger data type to the smaller data type variable, explicit typecasting will be required.

  - It is also known as narrowing (or) down casting

  - There may be a chance of loss of information in this type casting.


<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/Explicit%20TypeCasting.jpg)](https://github.com/ashwinkol/Notes/tree/main/)

</div>

---

# Conditional Statement In Java

In Java, conditional statements allow you to control the flow of your program based on certain conditions. There are mainly three types of conditional statements in Java: `if`, `else if`, and `else`. Additionally, Java provides a `switch` statement for more complex conditional branching.

1. **if Statement**:
   - The `if` statement evaluates a boolean expression and executes a block of code if the condition is true.
   - Syntax:
     ```java
     if (condition) {
         // code to be executed if the condition is true
     }
     ```
   - Example:
     ```java
     int x = 10;
     if (x > 5) {
         System.out.println("x is greater than 5");
     }
     ```

2. **if-else Statement**:
   - The `if-else` statement executes one block of code if the condition is true and another block if the condition is false.
   - Syntax:
     ```java
     if (condition) {
         // code to be executed if the condition is true
     } else {
         // code to be executed if the condition is false
     }
     ```
   - Example:
     ```java
     int x = 3;
     if (x % 2 == 0) {
         System.out.println("x is even");
     } else {
         System.out.println("x is odd");
     }
     ```

3. **if-else if-else Statement**:
   - The `if-else if-else` statement allows you to check multiple conditions and execute different blocks of code based on the result of those conditions.
   - Syntax:
     ```java
     if (condition1) {
         // code to be executed if condition1 is true
     } else if (condition2) {
         // code to be executed if condition2 is true
     } else {
         // code to be executed if all conditions are false
     }
     ```
   - Example:
     ```java
     int x = 0;
     if (x > 0) {
         System.out.println("x is positive");
     } else if (x < 0) {
         System.out.println("x is negative");
     } else {
         System.out.println("x is zero");
     }
     ```

4. **switch Statement**:
   - The `switch` statement evaluates an expression and executes the corresponding block of code based on the value of the expression.
   - Syntax:
     ```java
     switch (expression) {
         case value1:
             // code to be executed if expression equals value1
             break;
         case value2:
             // code to be executed if expression equals value2
             break;
         // more cases...
         default:
             // code to be executed if expression doesn't match any case
     }
     ```
   - Example:
     ```java
     int dayOfWeek = 3;
     switch (dayOfWeek) {
         case 1:
             System.out.println("Monday");
             break;
         case 2:
             System.out.println("Tuesday");
             break;
         // more cases...
         default:
             System.out.println("Invalid day");
     }
     ```

These conditional statements provide you with the flexibility to execute different blocks of code based on various conditions, making your programs more dynamic and responsive.


---




