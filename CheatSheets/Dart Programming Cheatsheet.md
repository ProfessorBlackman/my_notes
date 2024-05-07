## Table of Contents

1. [Basic Syntax](#basic-syntax)
2. [Variables](#variables)
3. [Data Types](#data-types)
4. [Control Flow](#control-flow)
5. [Functions](#functions)
6. [Functional Programming](#functional-programming)
7. [Collections](#collections)
8. [Classes and Objects](#classes-and-objects)
9. [Inheritance](#inheritance)
10. [Exceptions](#exceptions)

---

## Basic Syntax

```dart
// Single-line comment

/*
   Multi-line
   comment
*/

void main() {
  print("Hello, Dart!");
}
```

## Variables
```dart
var name = "John";         // Dynamic type inference
String lastName = "Doe";   // Explicit type declaration
final age = 30;            // Immutable variable
const PI = 3.1415;         // Compile-time constant
```
## Data Types

- `int`: Integer values
- `double`: Floating-point values
- `String`: Textual data
- `bool`: Boolean values
- `List`: Ordered collection
- `Map`: Key-value pairs
- `dynamic`: Dynamic type
- `var`: Type inference

## Control Flow
### Conditional Statement
```dart
if (condition) {
  // Code to execute if condition is true
} else if (anotherCondition) {
  // Code to execute if anotherCondition is true
} else {
  // Code to execute if neither condition is true
}
```

### Loops
```dart
for (var i = 0; i < 5; i++) {
  // Loop with a counter
}

while (condition) {
  // Loop while condition is true
}

do {
  // Loop at least once, then while condition is true
} while (condition);

```

## Functions
```dart
int add(int a, int b) {
  return a + b;
}

// Shorter syntax (Arrow function)
int multiply(int a, int b) => a * b;

// Optional named parameters
int divide({int a = 10, int b = 2}) {
  return a ~/ b;
}

// Function as a first-class citizen
int operate(int Function(int, int) op, int a, int b) {
  return op(a, b);
}
```

## Functional Programming
### Higher Order Functions
```dart
List<int> numbers = [1, 2, 3, 4, 5];

var doubledNumbers = numbers.map((n) => n * 2);

var evenNumbers = numbers.where((n) => n % 2 == 0);

var sum = numbers.reduce((a, b) => a + b);
```

## Closures
```dart
Function makeMultiplier(int multiplier) {
  return (int number) => number * multiplier;
}

var double = makeMultiplier(2);
var triple = makeMultiplier(3);
```

## Collections
### Lists
```dart
List<int> numbers = [1, 2, 3];
numbers.add(4);
numbers.remove(2);
numbers.forEach((number) => print(number));
```
### Maps
```dart
Map<String, int> ages = {
  'Alice': 25,
  'Bob': 30,
};
ages['Charlie'] = 22;
print(ages['Alice']);
```
### Classes and Objects
```dart
class Person {
  String name;
  int age;

  Person(this.name, this.age);

  void sayHello() {
    print("Hello, my name is $name and I am $age years old.");
  }
}

var person = Person("Alice", 25);
person.sayHello();
```
### Inheritance
```dart
class Student extends Person {
  String major;

  Student(String name, int age, this.major) : super(name, age);

  @override
  void sayHello() {
    print("Hi, I'm $name, a student majoring in $major.");
  }
}
```
### Exceptions
```dart
try {
  // Code that may throw an exception
} catch (e) {
  // Handle the exception
} finally {
  // Code that always runs
}
```