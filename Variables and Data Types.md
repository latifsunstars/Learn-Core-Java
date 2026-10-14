# Variables and Data Types
Let's dive into **variables** and **data types**, which are fundamental concepts in Java (and programming in general). 
Variables store data, and data types define what kind of data a variable can hold.

---

## **Step 1: What Are Variables?**
A **variable** is a named storage location in memory that holds a value. It has:
- A **name** (identifier).
- A **data type** (e.g., `int`, `String`).
- A **value** (the data it currently holds).

### **Example:**
```java
int age = 25;
String name = "Alice";
```

---

## **Step 2: Declaring Variables**
To declare a variable, you specify its type and name. Optionally, you can initialize it with a value.

### **Syntax:**
```java
<data_type> <variable_name> [= value];
```
- `data_type`: The type of data the variable will store (e.g., `int`, `String`).
- `variable_name`: A valid identifier (e.g., `age`, `name`).
- `= value`: Optional initialization.

### **Example:**
```java
int age;          // Declaration only (no value yet)
double price = 19.99;  // Declaration and initialization
boolean isJavaFun = true;
```

---

## **Step 3: Java Data Types**
Java data types are categorized into two groups:
1. **Primitive Data Types**: Built-in types for basic values.
2. **Reference (Non-primitive) Data Types**: Objects like `String`.

### **1. Primitive Data Types**
| Data Type | Size (bits) | Range / Description                          |
|-----------|-------------|----------------------------------------------|
| `byte`    | 8           | -128 to 127 (small integers)                |
| `short`   | 16          | -32,768 to 32,767                           |
| `int`     | 32          | -2,147,483,648 to 2,147,483,647             |
| `long`    | 64          | Larger integers (e.g., `long phoneNumber = 9876543210L;`) |
| `float`   | 32          | Decimals with single precision (e.g., `3.14f`)|
| `double`  | 64          | Decimals with double precision (default for floating-point) |
| `char`    | 16          | Single Unicode character (e.g., `'A'`, `'1'`) |
| `boolean` | 1           | `true` or `false`                           |

### **Example:**
```java
byte smallNumber = 100;
int age = 25;
long population = 7_000_000_000L; // Underscores for readability
double pi = 3.141592653589793;
float temperature = 98.6f;
char grade = 'A';
boolean isRaining = false;
```

---

### **2. Reference Data Types**
The most common reference type is `String`, which represents a sequence of characters.

### **Example:**
```java
String name = "Alice";
String message = "Hello, World!";
```

---

## **Step 4: Variable Scope and Lifetime**
- **Scope**: Where the variable can be accessed (e.g., inside a method or class).
- **Lifetime**: How long the variable exists in memory.

### **Example:**
```java
public class VariableScope {
    public static void main(String[] args) {
        int age = 25; // Local variable (visible only inside main)
        System.out.println(age);

        if (age > 18) {
            int votingAge = 18; // Scope is limited to the if-block
            System.out.println("Eligible to vote: " + votingAge);
        }
    }
}
```

---

## **Step 5: Type Conversion**
Java allows converting between data types, either implicitly (automatically) or explicitly.

### **1. Implicit Conversion (Widening)**
- Smaller type to larger type (e.g., `int` to `double`).

**Example:**
```java
int num = 10;
double decimalNum = num; // Implicit conversion from int to double
System.out.println(decimalNum); // Output: 10.0
```

### **2. Explicit Conversion (Narrowing)**
- Larger type to smaller type (e.g., `double` to `int`). Requires a cast.

**Example:**
```java
double decimalNum = 98.76;
int num = (int) decimalNum; // Explicit conversion (cast)
System.out.println(num);    // Output: 98 (truncates the decimal)
```

---

## **Step 6: Best Practices**
1. Always declare variables with meaningful names (e.g., `studentAge` instead of `x`).
2. Prefer `double` over `float` for precision unless memory is a constraint.
3. Initialize variables when you declare them to avoid undefined values.
4. Be mindful of variable scope to avoid unintended access.

---

## **Step 7: Hands-On Exercise**
Write a Java program that:
1. Declares variables for your name (`String`), age (`int`), and height (`double`).
2. Prints them in a formatted message like:
   ```
   Name: Alice, Age: 25, Height: 5.6
   ```

### **Solution:**
```java
public class MyInfo {
    public static void main(String[] args) {
        String name = "Alice";
        int age = 25;
        double height = 5.6;

        System.out.println("Name: " + name + ", Age: " + age + ", Height: " + height);
    }
}
```

---

## **Next Steps**
1. Practice declaring and using different data types.
2. Experiment with type conversion (e.g., converting `double` to `int`).
3. Learn about operators (`+`, `-`, `*`, `/`) in the next lesson.
