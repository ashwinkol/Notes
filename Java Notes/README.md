# Java Basic Elements

## Data Types And Literals

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

# Arithmetic Operators In Java

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

# Arithmetic Operator Precedence in Java


## Arithmetic Operator Precedence in Java

1. **Multiplication: `*`**
   - Multiplication has higher precedence than division, addition, and subtraction.

2. **Division: `/`**
   - Division has higher precedence than addition and subtraction, but lower precedence than multiplication.

3. **Addition: `+`**
   - Addition has higher precedence than subtraction.

4. **Subtraction: `-`**
   - Subtraction has the lowest precedence among arithmetic operators.


1. **Parentheses: `()`**
   - Parentheses have the highest precedence and are used to explicitly specify the order of operations.

2. **Unary Operators: `+`, `-`**
   - Unary plus (`+`) and unary minus (`-`) operators are applied to individual operands.

3. **Multiplication, Division, Modulus: `*`, `/`, `%`**
   - Multiplication (`*`), division (`/`), and modulus (`%`) operators have the same precedence and are evaluated from left to right.

4. **Addition and Subtraction: `+`, `-`**
   - Addition (`+`) and subtraction (`-`) operators have the same precedence and are evaluated from left to right.

### Example:

Consider the following expression:

```java
int result = 10 * 2 + 5 - 3 / 2;
```

In this expression:
1. `3 / 2` is evaluated first due to the higher precedence of multiplication, division, and modulus.
2. Then, `10 * 2`, `5`, and `-` are evaluated from left to right.
3. Finally, `+` and `-` are evaluated from left to right.

To make the order of operations explicit, you can use parentheses:

```java
int result = ((10 * 2) + 5) - (3 / 2);
```

This ensures that `10 * 2` and `3 / 2` are evaluated first due to the parentheses.

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

# Access Modifiers In Java

Access modifiers are keywords used in Java to define accessibility permissions.

## Different levels of Accessibility permissions:

Java supports 4 accessibility levels:

1. Only within the class
2. Only within the package
3. Outside the package but only in subclass by assigning the same subclass object
4. From all places of the project

## Accessibility modifier keywords:

To define the above 4 levels, we have 3 keywords:

1. **private Access Modifier - `private`**:

   Variables, Methods, and Constructors that are declared private can only be accessed within the declared class itself. The private access modifier is the most restrictive access level modifier. Classes and interfaces cannot be private. Variables declared private can be accessed outside the class if public getter methods are present in the class.

   Using the private modifier is the primary way that an object encapsulates itself and hides data from the outside world.

2. **protected Access Modifier - `protected`**:

   Variables, methods, and constructors declared protected in a superclass can be accessed only by subclasses in other packages or any class within the package of the protected members' class. The protected access modifier cannot be applied to classes and interfaces. Methods and fields can be declared protected, but methods and fields in an interface cannot be declared protected.

   Protected access gives the subclass a chance to use the helper method or variable while preventing a nonrelated class from using it.

3. **public Access Modifier - `public`**:

   A class, method, constructor, or interface declared public can be accessed from any other class. Therefore, fields, methods, and blocks declared inside a public class can be accessed from any class belonging to the Java Universe.

   However, if the public class we are trying to access is in a different package, then the public class still needs to be imported. Because of class inheritance, all public methods and variables of a class are inherited by its subclasses.

   
<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/AcsessModifires.jpg)](https://github.com/ashwinkol/Notes/tree/main/)

</div>


---

# Wrapper Classes in Java


The classes used to represent primitive values as objects are called wrapper classes. In the `java.lang` package, there are 8 wrapper classes, one for each primitive type, to represent them as objects. Among them, 6 wrapper classes represent number type values and are known as number wrapper classes. These 6 number wrapper classes are subclasses of the abstract class `Number`. This class has `xxxValue()` methods to read primitive values from wrapper class objects. Except for `byteValue()` and `shortValue()`, the remaining 4 methods are abstract methods as they are methods of an abstract class. These 6 methods are implemented in all 6 number wrapper classes by returning the current object's internal primitive value.

Wrapper classes in Java are used to represent primitive data types as objects. They provide a way to treat primitive data types as objects, enabling various operations such as comparison, storage in collections, and passing as arguments in methods.

### List of Wrapper Classes:

1. **Byte**: `java.lang.Byte`
2. **Short**: `java.lang.Short`
3. **Integer**: `java.lang.Integer`
4. **Long**: `java.lang.Long`
5. **Float**: `java.lang.Float`
6. **Double**: `java.lang.Double`
7. **Character**: `java.lang.Character`
8. **Boolean**: `java.lang.Boolean`

Wrapper classes provide methods to convert primitive data types to and from strings, perform arithmetic operations, and check for various properties of the values they represent.

For example, you can create an `Integer` object from an `int` primitive data type like this:

```java
Integer number = Integer.valueOf(10);
```

And you can convert an `Integer` object back to an `int` primitive data type like this:

```java
int value = number.intValue();
```

Wrapper classes are commonly used when working with collections like `ArrayList` or `HashMap`, as these collections require objects rather than primitive data types. Additionally, wrapper classes are useful for handling null values, as primitive data types cannot be null but wrapper classes can.

<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/WrapperClass.png )](https://github.com/ashwinkol/Notes/tree/main/)

</div>


### Need of Wrapper Classes:

Wrapper classes are primarily used in projects to perform conversion operations. There are 6 conversion operations:

1. **AutoBoxing**: Converting a primitive type into a wrapper class object automatically.

2. **AutoUnboxing**: Converting a wrapper class object into a primitive type automatically.

### AutoBoxing and AutoUnboxing:

As per AutoBoxing and AutoUnBoxing, primitive values can be assigned to wrapper class referenced variables and wrapper class objects can be assigned to primitive variables directly. The required conversion is done automatically by the compiler.

**Q**: Who performs AutoBoxing and UnBoxing, the Compiler or JVM?

**Ans**: AutoBoxing and AutoUnBoxing are performed by the Compiler based on the primitive literal. This feature requires code added to the compiler software. Therefore, the JVM does not handle this feature.

**AutoBoxing**:
Let's understand how the compiler performs AutoBoxing in the following statement:

```java
Integer io = 50;
```

In the above line, the compiler converts `Integer io` to `Integer.valueOf(50)`, converting the int literal 50 to an Integer object. So, in the ".class" file, we do not have 50 as an int literal; it is stored as an Integer object. Thus, the JVM processes the value 50 as an Integer object.

**Q**: On what basis does the compiler convert primitive values to wrapper class objects?

**Ans**: The compiler converts primitive values to wrapper class objects based on the type of primitive value. For example, `int` is converted to `Integer`, `float` to `Float`, `char` to `Character`, and `boolean` to `Boolean`.

---







