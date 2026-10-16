# **Operators and Expressions in Java**

Operators are symbols that perform operations on variables and values. They allow you to manipulate data, perform calculations, and make decisions in your programs. Let's explore the different types of operators in Java.

---

## **Step 1: Types of Operators**
Java operators are categorized as follows:

1. **Arithmetic Operators**: Perform mathematical operations.
2. **Relational (Comparison) Operators**: Compare values.
3. **Logical (Boolean) Operators**: Combine boolean expressions.
4. **Bitwise Operators**: Work on bits.
5. **Assignment Operators**: Assign values to variables.
6. **Ternary Operator**: A shorthand for `if-else`.
7. **Other Operators**: Increment (`++`), Decrement (`--`), etc.

---

## **Step 2: Arithmetic Operators**
Used for mathematical operations like addition, subtraction, multiplication, and division.

| Operator | Description          | Example               |
|----------|----------------------|-----------------------|
| `+`      | Addition             | `a + b`               |
| `-`      | Subtraction          | `a - b`               |
| `*`      | Multiplication       | `a * b`               |
| `/`      | Division (floating-point result) | `a / b`       |
| `%`      | Modulus (remainder)  | `a % b`               |

### **Example:**
```java
public class ArithmeticOperators {
    public static void main(String[] args) {
        int a = 10, b = 3;

        System.out.println("Addition: " + (a + b)); // 13
        System.out.println("Subtraction: " + (a - b)); // 7
        System.out.println("Multiplication: " + (a * b)); // 30
        System.out.println("Division: " + (a / b)); // 3 (integer division)
        System.out.println("Modulus: " + (a % b)); // 1 (remainder)

        double c = a, d = b;
        System.out.println("Floating-point Division: " + (c / d)); // 3.333...
    }
}
```

### **Key Notes:**
- If both operands are `int`, division (`/`) performs **integer division** (e.g., `10 / 3 = 3`).
- To get a floating-point result, cast one operand to `double`:
  ```java
  double result = (double)a / b; // 3.333...
  ```

---

## **Step 3: Relational (Comparison) Operators**
Compare two values and return `true` or `false`.

| Operator | Description          | Example               |
|----------|----------------------|-----------------------|
| `==`     | Equal to             | `a == b`              |
| `!=`     | Not equal to         | `a != b`              |
| `>`      | Greater than         | `a > b`               |
| `<`      | Less than            | `a < b`               |
| `>=`     | Greater than or equal| `a >= b`              |
| `<=`     | Less than or equal   | `a <= b`              |

### **Example:**
```java
int x = 10, y = 20;

System.out.println(x == y); // false
System.out.println(x != y); // true
System.out.println(x > y); // false
System.out.println(y >= x); // true
```

---

## **Step 4: Logical (Boolean) Operators**
Combine boolean expressions.

| Operator | Description          | Example               |
|----------|----------------------|-----------------------|
| `&&`     | Logical AND          | `a > 0 && a < 10`     |
| `||`     | Logical OR           | `a > 0 || a < 5`      |
| `!`      | Logical NOT          | `!(a == b)`           |

### **Example:**
```java
boolean isRaining = true;
boolean isCold = false;

System.out.println(isRaining && isCold); // false (both must be true)
System.out.println(isRaining || isCold); // true (either can be true)
System.out.println(!isRaining); // false (inverts the value)
```

---

## **Step 5: Assignment Operators**
Assign values to variables.

| Operator | Description          | Example               |
|----------|----------------------|-----------------------|
| `=`      | Assign               | `a = 10`              |
| `+=`     | Add and assign       | `a += 5` (same as `a = a + 5`) |
| `-=`     | Subtract and assign  | `a -= 3`              |
| `*=`     | Multiply and assign  | `a *= 2`              |
| `/=`     | Divide and assign    | `a /= 2`              |
| `%=`     | Modulus and assign   | `a %= 4`              |

### **Example:**
```java
int a = 5;
a += 3; // a is now 8 (same as a = a + 3)
System.out.println(a);
```

---

## **Step 6: Increment (`++`) and Decrement (`--`) Operators**
- `++` increases the value of a variable by 1.
- `--` decreases the value of a variable by 1.

| Operator | Description          | Example               |
|----------|----------------------|-----------------------|
| `a++`    | Post-increment       | Increment after use   |
| `++a`    | Pre-increment        | Increment before use  |
| `a--`    | Post-decrement       | Decrement after use   |
| `--a`    | Pre-decrement        | Decrement before use  |

### **Example:**
```java
int b = 5;
System.out.println(b++); // Output: 5 (post-increment)
System.out.println(b);   // Now b is 6

System.out.println(++b); // Output: 7 (pre-increment)
```

---

## **Step 7: Ternary Operator (`?:`)**
A shorthand for `if-else`.

### **Syntax:**
```java
<condition> ? <expression_if_true> : <expression_if_false>
```

### **Example:**
```java
int age = 18;
String status = (age >= 18) ? "Adult" : "Minor";
System.out.println(status); // Adult
```

---

## **Step 8: Bitwise Operators**
Work on bits and are used for low-level operations.

| Operator | Description          |
|----------|----------------------|
| `&`      | AND                  |
| `|`      | OR                   |
| `^`      | XOR (exclusive OR)   |
| `~`      | NOT (bitwise complement) |
| `<<`     | Left shift           |
| `>>`     | Right shift          |

### **Example:**
```java
int x = 5; // Binary: 0101
int y = 3; // Binary: 0011

System.out.println(x & y); // AND: 0001 (1)
System.out.println(x | y); // OR:  0111 (7)
```

---

## **Step 9: Hands-On Exercises**
1. Write a program to calculate the area of a rectangle (`length * width`).
2. Compare two numbers and print whether they are equal, greater, or smaller.
3. Use the ternary operator to check if a number is even or odd.

### **Solution for Exercise 1:**
```java
public class AreaCalculator {
    public static void main(String[] args) {
        int length = 5, width = 4;
        int area = length * width;
        System.out.println("Area of the rectangle: " + area);
    }
}
```

### **Solution for Exercise 2:**
```java
int num1 = 10, num2 = 20;

if (num1 == num2) {
    System.out.println("Equal");
} else if (num1 > num2) {
    System.out.println(num1 + " is greater than " + num2);
} else {
    System.out.println(num2 + " is greater than " + num1);
}
```

### **Solution for Exercise 3:**
```java
int number = 7;
String result = (number % 2 == 0) ? "Even" : "Odd";
System.out.println(number + " is " + result);
```

---

## **Step 10: Best Practices**
1. Use meaningful variable names to reflect their purpose.
2. Be cautious with operator precedence (e.g., `*` has higher precedence than `+`).
3. Use parentheses `( )` to group operations for clarity and correctness.

---

## **Next Steps**
- Practice using operators in small programs.
- Learn about control statements (`if`, `else`, `switch`) next, which rely heavily on relational/logical operators.
