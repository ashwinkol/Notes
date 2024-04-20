# Java Basic Elements

# Variable in Java

### Understanding Variable and Method Execution in Java

### Variable Execution vs. Method Execution

In Java, there's a distinction between executing a variable and executing a method:

**Executing a Variable:**

Executing a variable involves creating a memory location for the variable with an initialized value. The Java Virtual Machine (JVM) automatically executes variables when the variable creation statement appears in the program, i.e., by reading its value.

**Executing a Method:**

Executing a method means executing the logic defined within the method. The JVM does not execute method logic automatically. It executes the method only when the method calling statement appears, not merely by defining the method logic.


**Q.** What is the difference between executing a variable and executing a method?

Executing a variable: Executing a variable means creating variable memory location wit Initialized value. Jvm executes variables automatically when variable creation statemer appears in the program. l.e., reading its value.

Executing a method: It means executing method logic. Jvm does not execute method log Buting jadically. It executes method only when that method calling statement appears and not b using just definition l.e., executing that method logic

---

## Types of Variables

Based on class scopes, variables in Java are divided into three types:

### Local Variables

- Local variables are declared in methods, constructors, or blocks.
- They are created when the method, constructor, or block is entered and destroyed once it exits.
- Access modifiers cannot be used for local variables, and they are visible only within the declared method, constructor, or block.
- Local variables are implemented at the stack level internally.
- They must be declared and initialized before use, as there is no default value for them.

### Instance Variables


Instance variables are declared within a class directly, but not outside a method, constructor, or any block. When space is allocated for an object in the heap, a slot for each instance variable value is created.

Instance variables are created when an object is created with the use of the keyword 'new' and destroyed when the object is destroyed. They hold values that must be referenced by more than one method, constructor, or block, or essential parts of an object, allowing the state to be present throughout the class.

Instance variables can be declared at the class level before or after use. Access modifiers can be given for instance variables. Normally, it is recommended to make these variables private (access level), however, visibility for subclasses can be given for these variables with the use of access modifiers.

Instance variables have default values: 0 for numbers, false for Booleans, and null for object references. Values can be assigned during declaration or within the constructor.

Instance variables can be accessed directly by calling the variable name inside the class. However, within static methods and different classes (when instance variables are given accessibility), they should be called using the fully qualified name: `ObjectReference.VariableName`.

- Instance variables are declared within a class but not within a method, constructor, or block.
- They are created when an object is created and destroyed when the object is destroyed.
- Instance variables hold values referenced by more than one method, constructor, or block and are present throughout the class.
- They can be accessed directly within the class and are typically recommended to be private.
- Instance variables have default values (0 for numbers, false for Booleans, null for object references), which can be assigned during declaration or within the constructor.



### Class/Static Variables

- Class or static variables are shared among all instances of a class.
- They are declared using the `static` keyword and retain their values throughout the class's lifetime.
- Class variables can be accessed directly using the class name and are typically recommended to be private.




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

## AutoBoxing and AutoUnboxing:

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

## Auto Promotion 


In Java, autopromotion refers to the automatic conversion of lower-sized primitive data types to higher-sized ones when they are involved in expressions or assignments. This conversion is done by the Java compiler to prevent data loss and ensure that the operation is carried out using the higher precision data type.

```java
class Test {
public static void main(String[] args) {
    byte a = 10;
    byte b = 20;
    
    byte c = a + b;
    
    System.out.println(c);
   }
}

```


<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/ImplicitTypeCasting.jpg)](https://github.com/ashwinkol/Notes/tree/main/)

</div>

---
# Methods And Types of Method

Need To added
---

# Constructor In Java

## Definition

A constructor is a special method in object-oriented programming languages used for creating and initializing objects. In Java, a constructor's role is limited to initializing objects, while the `new` keyword is responsible for creating objects. In languages like C++, a constructor both creates and initializes objects.

## Rules for Defining Constructors

1. Constructor name should be the same as the class name.
2. Constructors should not contain a return type.
3. Constructors should not contain modifiers.
4. A return statement with a value is not allowed in constructors.

## Constructor Creation Syntax

```java
class Example {
    Example() {
        // All Java legal statements are allowed 
        // except return statement with value
        System.out.println("constructor");
    }
}
```

## Rule for Calling Constructors
Constructors must be called using the `new` keyword, otherwise, it leads to a compiler time error.

**Q.** Can We Define a Method with the Same Class Name?

Yes, it is allowed to define a method with the same class name. However, it is not recommended as per coding standards.

- When we place return type in the construstor prototype compiler and jvm condider it as a method.


**Q.** How compiler and jvm can differentiate constructor and method definitions  if both have same class name?

By using return type, if there is a return type it is considered as method else it is considered as a constructor.

**Q.** How compiler and jvm can differentiate constructor and method invocations if both have same class name?

By using new keyword, if new keyword is used in calling then constructor is executed, else method is executed.

**Q.** Can we declare constructor as private?

Yes, we can declare constructor as private. All four accessibility modifiers are allowed for constructor. We should declare constructor as private to not allow the user to create object from outside of class. Basically we will declare constructor as private to implement Singleton design pattern. 

**Q.** Is constructor definition mandatory in class?

No, it is optional .If we do not define constructor compiler defines constructor.

## Types of Constructors
 Java supports three types of constructors:

1. Default constructor

2. No-argument or non-parameterized constructor

3. Parameterized constructor.

The default constructor, generated by the compiler, has no parameters and logic except for the super() call. The no-argument constructor is developer-generated without parameters. The parameterized constructor, also developer-generated, includes parameters and logic.

**Q.** Why is the Compiler-Generated Constructor Called the Default Constructor?

- Because it obtain all its default properties from its class they are:

1. Its accessibility modifier is the same as its class.
2. Its name is the same as its class name.
3. It does not have parameters and logic.


**Q.** What is the Diff. between no-argument and default constructor?

<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/Constructor.jpg)](https://github.com/ashwinkol/Notes/tree/main/)

</div>

## Constructor Chaining in Java

Constructor chaining is a technique in Java where a constructor calls another constructor of the same class or its parent class. This allows for code reuse and helps in avoiding duplication of code.

## How Constructor Chaining Works

1. Constructor chaining can occur within the same class or between parent and child classes.
2. In the same class, one constructor can call another constructor using `this()` keyword.
3. In the case of inheritance, a subclass constructor can call a constructor of its superclass using `super()` keyword.
4. The chaining should be the first statement in the constructor body.
5. By default, if no constructor is explicitly called, Java inserts a call to the superclass's default constructor (`super()`).

## Examples: 

```java
class Parent {
    Parent() {
        System.out.println("Parent default constructor");
    }

    Parent(int x) {
        System.out.println("Parent parameterized constructor with value " + x);
    }
}

class Child extends Parent {
    Child() {
        super(); // Call to superclass's default constructor
        System.out.println("Child default constructor");
    }

    Child(int y) {
        super(y); // Call to superclass's parameterized constructor
        System.out.println("Child parameterized constructor with value " + y);
    }
}

public class ConstructorChaining {
    public static void main(String[] args) {
        Child child1 = new Child(); // Output: Parent default constructor, Child default constructor
        Child child2 = new Child(10); // Output: Parent parameterized constructor with value 10, Child parameterized constructor with value 10
    }
}
```

## Introduction to Non-Static Blocks in Java

In Java, non-static blocks are used for initializing instance variables and performing additional setup actions when objects of a class are created. These blocks are executed every time an object of the class is instantiated.

## Types of Non-Static Blocks

There are two types of non-static blocks in Java:

1. **Initialization Block:**
   - Also known as an instance initialization block.
   - Written within curly braces `{}` without any method name or access specifier.
   - Executed whenever an instance of the class is created.
   - Useful for performing common initialization tasks for all constructors.

2. **Constructor:**
   - A special type of method that has the same name as the class and is used to initialize objects.
   - Can contain custom initialization logic specific to each constructor.
   - Executed after the instance initialization block.

## Key Points

- Non-static blocks are mainly used for initializing instance variables and executing additional setup logic when objects are created.
- Instance initialization blocks are executed before constructors, while constructors are executed after them.
- Non-static blocks cannot be directly invoked like methods; they are automatically executed during object creation.

## Example

```java
public class NonStaticBlocksDemo {
    // Instance initialization block
    {
        System.out.println("Instance initialization block executed");
    }

    // Constructor
    public NonStaticBlocksDemo() {
        System.out.println("Constructor executed");
    }

    // Main method
    public static void main(String[] args) {
        NonStaticBlocksDemo obj = new NonStaticBlocksDemo();
    }
}
```
```
Output:
Instance initialization block executed
Constructor executed
```

## What jvm does internally when an object is created?

- Object creation process: 

When we create an object -first the control is sent to invoked constructor, but its logic will not be executed. Instead non-static variables and non-static blocks are executed first in the order they are defined from top to bottom, then constructor logic is executed.

If all non-static variables and non-static blocks object creation is completed.


## Responsibilities of new keyword and constructor in creating object 

responsibility of new keyword is :

#### In identification phase: 

 It creates non-static variables with default values in heap area in continuous memory locations and also identifies non-static blocks.

#### In execution phase: 

- It executes variables and non-static blocks in the order they are defined, which means it is initialized as non-static variable with assigned values and executes non-static block logic in JSA(JavaStackArea) by creating separate stack frame.

- After execution of non-static variables and non-static blocks new keyword sends control into the invoked constructor with this object reference to complete object initialization with user given values.

- The responsibility of constructor is initializing a non-static variables which means object with developer or user given values as per its logic.

- Then finally new keyword returns object reference to calling area, then it is stored in destination referenced variable.

---

# Java Clone Deep Copy and Shallow Copy 

Clone is a Greek word meaning "branch". In java, though clone is 'intended' to produce a copy of the same object it is not guaranteed. Clone comes with lots of if's and buts. Hence my first advice is to not depend on clones

## Shallow Copy : 
Shallow copy is a bit-wise copy of an object. A new object is created that has an exact copy of the values in the original object. If any of the fields of the object refers to other objects, just the reference address are copied i.e only the memory address is copied.


<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/ShalloCopy.jpg)](https://github.com/ashwinkol/Notes/tree/main/)

</div>

In this figure, the MainObject1 have fields "field1" of int type, and "ContainObject1" of ContainObject type. When you do a shallow copy of MainObject1, MainObject2 is created with "field3" containing the copied value of "field1" and still pointing to ContainObject1 itself. Here you will find that as field1 is of primitive type, the values of it are copied to field3 but ContainedObject1 is an object, so MainObject2 is still pointing to ContainObject1. Therefore any changes made to ContainObject1 in MainObject1 will reflect in MainObject2.


## Deep Copy :

A deep copy copies all fields, and makes copies of dynamically allocated memory pointed to, by the fields. A deep copy occurs when an object is copied along with the objects to which it refers

<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/DeepCopy.jpg)](https://github.com/ashwinkol/Notes/tree/main/)

</div>


In this figure, the MainObject1 have fields "field1" of int type, and "ContainObject1" of ContainObject type. When you do a deep copy of MainObject1, MainObject2 is created with "field3" containing the copied value of "field1" and "ContainObject2" containing the copied value of ContainObject1.So any changes made to ContainObject1 in MainObject1 will not reflect in MainObject2

### Differences Between Shallow Copy and Deep Copy
<div style="text-align:center">

[![Java Data Types](/Java%20Notes/images/deepCopyVsShallowCopy.png)](https://github.com/ashwinkol/Notes/tree/main/)

</div>


## Example: 

```java
class Employee implements Cloneable {
    private String name;
    private String designation;

    public Employee() {
        this.setDesignation("Programmer");
    }

    public String getDesignation() {
        return designation;
    }

    public void setDesignation(String designation) {
        this.designation = designation;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    @Override
    public Object clone() throws CloneNotSupportedException {
        /*
        Employee copyObj = new Employee();
        copyObj.setDesignation(this.designation);
        copyObj.setName(this.name);
        return copyObj;
        */
        return super.clone();
    }
}

public class CloneExample {
    public static void main(String arg[]) {
        Employee jwz = new Employee();
        jwz.setName("malla nareshit");

        try {
            Employee joel = (Employee) jwz.clone();
            System.out.println(joel.getName());
            System.out.println(joel.getDesignation());
        } catch (CloneNotSupportedException cnse) {
            System.out.println("Cloneable should be implemented. " + cnse);
        }
    }
}

```

```
Output:
malla nareshit
Programmer
```
---