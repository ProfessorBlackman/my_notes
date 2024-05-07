# Java Programming Cheatsheet

## Basics

### Data Types
- `int`: Integer data type
- `double`: Double-precision floating-point data type
- `char`: Character data type
- `boolean`: Boolean data type
- `String`: A sequence of characters

### Variables
```java
int age = 25;
double price = 19.99;
char grade = 'A';
boolean isActive = true;
String name = "John";
```

### Operators
- Arithmetic: `+`, `-`, `*`, `/`, `%`
- Assignment: `=`, `+=`, `-=`, `*=`, `/=`, `%=`
- Comparison: `==`, `!=`, `<`, `>`, `<=`, `>=`
- Logical: `&&` (AND), `||` (OR), `!` (NOT)

## Control Flow

### Conditional Statements
```java
if (condition) {
    // code to execute if condition is true
} else if (anotherCondition) {
    // code to execute if anotherCondition is true
} else {
    // code to execute if no condition is true
}
```

### Loops
- `for` loop:
```java
for (int i = 0; i < 5; i++) {
    // code to repeat
}
```
- `while` loop:
```java
while (condition) {
    // code to repeat
}
```
- `do-while` loop:
```java
do {
    // code to repeat
} while (condition);
```

## Arrays

### Declaration and Initialization
```java
int[] numbers = { 1, 2, 3, 4, 5 };
String[] names = new String[3];
names[0] = "Alice";
names[1] = "Bob";
names[2] = "Charlie";
```

### Accessing Array Elements
```java
int firstNumber = numbers[0];
String firstName = names[0];
```

## Functions

### Method Declaration
```java
public returnType methodName(parameterType parameter) {
    // method body
    return returnValue;
}
```

### Example Method
```java
public int add(int a, int b) {
    return a + b;
}
```

## Classes and Objects

### Class Declaration
```java
public class ClassName {
    // fields (attributes)
    dataType fieldName;

    // constructor
    public ClassName(dataType initialValue) {
        fieldName = initialValue;
    }

    // methods
    public returnType methodName(parameterType parameter) {
        // method body
    }
}
```

### Object Creation
```java
ClassName objectName = new ClassName(initialValue);
```

### Inheritance
```java
class ChildClass extends ParentClass {
    // additional fields and methods
}
```

### Polymorphism
```java
ParentClass obj1 = new ChildClass();
```

### Interfaces
```java
interface MyInterface {
    void method1();
    int method2();
}
```

## Exception Handling

### Try-Catch Block
```java
try {
    // code that might throw an exception
} catch (ExceptionType exception) {
    // code to handle the exception
} finally {
    // code that runs regardless of whether an exception was caught
}
```

## Input and Output

### Console Input
```java
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);
String input = scanner.nextLine();
int number = scanner.nextInt();
```

### Console Output
```java
System.out.println("Hello, World!");
System.out.printf("Value: %d\n", number);
```