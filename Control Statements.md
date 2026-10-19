# **Control Statements in Java**

Control statements allow you to control the flow of your program's execution based on conditions. They help you decide whether to execute certain blocks of code or repeat actions. Let's explore them step by step.

---

## **Step 1: Types of Control Statements**
Java supports the following types of control statements:

1. **Conditional Statements**:
   - `if`
   - `else if` (optional)
   - `else`
   - `switch`

2. **Looping Statements**:
   - `for`
   - `while`
   - `do-while`

3. **Jump Statements** (transfer control):
   - `break`
   - `continue`
   - `return`

---

## **Step 2: Conditional Statements**
Conditional statements execute different blocks of code based on conditions.

### **1. `if` Statement**
Executes a block of code if a condition is true.

#### **Syntax:**
```java
if (condition) {
    // Code to execute if condition is true
}
```

#### **Example:**
```java
int age = 20;

if (age >= 18) {
    System.out.println("You are eligible to vote.");
}
```

---

### **2. `else` Statement**
Used with `if` to execute a block of code if the condition is false.

#### **Syntax:**
```java
if (condition) {
    // Code to execute if condition is true
} else {
    // Code to execute if condition is false
}
```

#### **Example:**
```java
int age = 15;

if (age >= 18) {
    System.out.println("You are eligible to vote.");
} else {
    System.out.println("You are not eligible to vote yet.");
}
```

---

### **3. `else if` Statement**
Used to check multiple conditions.

#### **Syntax:**
```java
if (condition1) {
    // Code for condition1
} else if (condition2) {
    // Code for condition2
} else {
    // Default code (executes if all conditions are false)
}
```

#### **Example:**
```java
int score = 85;

if (score >= 90) {
    System.out.println("Grade: A");
} else if (score >= 80) {
    System.out.println("Grade: B");
} else if (score >= 70) {
    System.out.println("Grade: C");
} else {
    System.out.println("Grade: F");
}
```

---

### **4. `switch` Statement**
Executes a block of code based on the value of an expression.

#### **Syntax:**
```java
switch (expression) {
    case value1:
        // Code to execute if expression == value1
        break;
    case value2:
        // Code to execute if expression == value2
        break;
    default:
        // Default code (executes if no cases match)
}
```

#### **Example:**
```java
int day = 3;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    default:
        System.out.println("Weekend or invalid day");
}
```

#### **Key Notes:**
- `break` is used to exit the `switch` block. Without it, execution will "fall through" to the next case.
- Java supports `String` as a valid expression in `switch` (from Java 7 onwards).

---

## **Step 3: Looping Statements**
Looping statements allow you to execute a block of code repeatedly.

### **1. `for` Loop**
Executes a block of code a specific number of times.

#### **Syntax:**
```java
for (initialization; condition; update) {
    // Code to execute in each iteration
}
```

#### **Example: Print numbers from 1 to 5**
```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

#### **Example: Iterate through an array**
```java
String[] fruits = {"Apple", "Banana", "Cherry"};

for (int i = 0; i < fruits.length; i++) {
    System.out.println(fruits[i]);
}
```

---

### **2. `while` Loop**
Executes a block of code while the condition is true.

#### **Syntax:**
```java
while (condition) {
    // Code to execute while condition is true
}
```

#### **Example: Print numbers from 1 to 5**
```java
int i = 1;
while (i <= 5) {
    System.out.println(i);
    i++;
}
```

---

### **3. `do-while` Loop**
Similar to `while`, but executes the block of code at least once before checking the condition.

#### **Syntax:**
```java
do {
    // Code to execute in each iteration
} while (condition);
```

#### **Example: Print numbers from 1 to 5**
```java
int i = 1;
do {
    System.out.println(i);
    i++;
} while (i <= 5);
```

---

## **Step 4: Jump Statements**

### **1. `break` Statement**
Exits a loop or `switch` statement immediately.

#### **Example with `for`:**
```java
for (int i = 1; i <= 10; i++) {
    if (i == 6) {
        break; // Exit the loop when i is 6
    }
    System.out.println(i);
}
```

#### **Example with `switch`:**
```java
int day = 5;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    default:
        System.out.println("Invalid day");
}
```

---

### **2. `continue` Statement**
Skips the current iteration of a loop and continues with the next one.

#### **Example:**
```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue; // Skip printing 3
    }
    System.out.println(i);
}
```

**Output:**
```
1
2
4
5
```

---

### **3. `return` Statement**
Exits the current method and returns a value to the caller.

#### **Example:**
```java
public class Example {
    public static int findMax(int a, int b) {
        if (a > b) {
            return a;
        } else {
            return b;
        }
    }

    public static void main(String[] args) {
        System.out.println(findMax(5, 10)); // Output: 10
    }
}
```

---

## **Step 5: Hands-On Exercises**

### **Exercise 1:**
Write a program to print the first 10 even numbers using a `for` loop.

#### **Solution:**
```java
public class EvenNumbers {
    public static void main(String[] args) {
        for (int i = 2; i <= 20; i += 2) {
            System.out.println(i);
        }
    }
}
```

---

### **Exercise 2:**
Write a program to calculate the sum of numbers from 1 to 10 using a `while` loop.

#### **Solution:**
```java
public class SumNumbers {
    public static void main(String[] args) {
        int sum = 0;
        int i = 1;

        while (i <= 10) {
            sum += i; // Equivalent to sum = sum + i;
            i++;
        }

        System.out.println("Sum: " + sum);
    }
}
```

---

### **Exercise 3:**
Write a program that asks the user for their age and prints whether they are a child, teenager, or adult using `if-else`.

#### **Solution:**
```java
import java.util.Scanner;

public class AgeChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();

        if (age < 13) {
            System.out.println("You are a child.");
        } else if (age >= 13 && age < 20) {
            System.out.println("You are a teenager.");
        } else {
            System.out.println("You are an adult.");
        }
    }
}
```

---

### **Exercise 4:**
Write a program that prints the days of the week using a `switch` statement.

#### **Solution:**
```java
public class DaysOfWeek {
    public static void main(String[] args) {
        int day = 3; // Let's say today is Wednesday

        switch (day) {
            case 1:
                System.out.println("Monday");
                break;
            case 2:
                System.out.println("Tuesday");
                break;
            case 3:
                System.out.println("Wednesday");
                break;
            case 4:
                System.out.println("Thursday");
                break;
            case 5:
                System.out.println("Friday");
                break;
            default:
                System.out.println("Weekend or invalid day");
        }
    }
}
```

---

## **Step 6: Best Practices**
1. Use `if-else` for conditions with multiple branches.
2. Use `switch` when you have multiple discrete values to check (e.g., days of the week, menu options).
3. Always include `break` in `switch` cases unless you intentionally want fall-through behavior.
4. Use `for` loops when you know the number of iterations in advance.
5. Use `while` or `do-while` for conditions where the number of iterations is not known beforehand.
6. Avoid infinite loops by ensuring your loop condition eventually becomes false.

---

## **Next Steps**
- Practice writing programs using control statements (e.g., simple calculators, number games).
- Learn about methods (functions) next, which can encapsulate logic and make your code reusable.
- Explore exception handling to handle unexpected situations gracefully.
