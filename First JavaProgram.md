# First Java Program: Write a simple "Hello, World!" program

Let's write your first Java program step by step. This will be a classic **"Hello, World!"** program, which is the traditional starting point for learning any programming language.

---

## **Step 1: Set Up Your Environment**
Before writing the code, ensure you have:
1. **Java Development Kit (JDK)** installed.
   - Download it from [Oracle's official website](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Verify the installation by running these commands in your terminal/command prompt:
   ```bash
   java -version
   javac -version
   ```
   - `java` is used to run Java programs.
   - `javac` is the compiler that converts `.java` files into bytecode (`.class` files).

---

## **Step 2: Write the "Hello, World!" Program**
Open a text editor or an IDE (like Notepad++, VS Code, IntelliJ IDEA, etc.).

### **Code:**
```java
// This is a single-line comment in Java

/*
   This is a multi-line comment.
   It can span across multiple lines.
*/

public class HelloWorld {
    // The main method is the entry point of the program
    public static void main(String[] args) {
        // Print "Hello, World!" to the console
        System.out.println("Hello, World!");
    }
}
```

### **Explanation:**
1. **`//` and `/* ... */`**:
   - These are comments in Java. They are ignored by the compiler.
   - Useful for explaining code or temporarily disabling parts of it.

2. **`public class HelloWorld`**:
   - Every Java program must have a class (a blueprint for objects).
   - The filename **must match the public class name** (e.g., `HelloWorld.java`).

3. **`main` Method**:
   - This is the entry point of the program. Execution starts here.
   - Signature: `public static void main(String[] args)`.

4. **`System.out.println()`**:
   - Prints the given string to the console and adds a new line (`ln` stands for "line").
   - `System` is a class, `out` is a static variable of type `PrintStream`, and `println` is a method.

---

## **Step 3: Save the File**
- Save the file as `HelloWorld.java`.
- Ensure the filename matches the public class name exactly (case-sensitive).

---

## **Step 4: Compile and Run the Program**
1. Open your terminal or command prompt.
2. Navigate to the directory where you saved `HelloWorld.java`:
   ```bash
   cd path/to/your/folder
   ```
3. Compile the program using `javac`:
   ```bash
   javac HelloWorld.java
   ```
   - This will generate a `HelloWorld.class` file (bytecode).

4. Run the compiled program:
   ```bash
   java HelloWorld
   ```

### **Expected Output:**
```
Hello, World!
```

---

## **Step 5: Troubleshooting**
- If you see an error like `error: class, interface, or enum expected`, ensure:
  - The filename matches the public class name.
  - There are no typos in the code.
- If you get a "Java not found" error, reinstall JDK and add it to your system's PATH.

---

## **Next Steps**
1. Experiment with the program by adding more `System.out.println()` statements.
2. Try printing variables:
   ```java
   public class HelloWorld {
       public static void main(String[] args) {
           String name = "Alice";
           System.out.println("Hello, " + name + "!");
       }
   }
   ```
3. Learn about data types and variables in the next lesson.
