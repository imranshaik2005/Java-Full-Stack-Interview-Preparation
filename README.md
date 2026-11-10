# Java-Full-Stack-Interview-Preparation
Daily Java Full Stack Developer interview preparation, coding practice, and technical questions.
# 🚀 Day 1 – Java Fundamentals | Interview Preparation

Welcome to Day 1 of my Java Full Stack Developer interview preparation.

This document contains important Java fundamentals, simple explanations, code examples, interview-ready answers, and possible follow-up questions.

## 📚 Technical Interview Questions

### 1. What is Java?

**Definition:**

Java is a high-level, object-oriented, class-based programming language used to develop desktop, web, mobile, and enterprise applications.

**Important Concepts:**

- **Programming Language:** A language used to give instructions to a computer.
- **High-Level Language:** A language that is easier for humans to read and understand.
- **Object-Oriented Programming (OOP):** A programming approach based on classes and objects.
- **Platform Independent:** Java bytecode can run on any system that has a compatible JVM.

**How Java Works:**

1. Write Java code in a `.java` file.
2. The Java compiler converts it into bytecode (`.class` file).
3. The JVM executes the bytecode.

**Interview Answer:**

Java is a high-level, object-oriented, and platform-independent programming language. It is widely used for developing web applications, enterprise applications, and Android applications.

**Follow-up Questions:**

- Who developed Java?
- Why is Java platform independent?
- What is bytecode?
- Is Java purely object-oriented?

---

### 2. Difference Between JDK, JRE, and JVM

| Term | Full Form | Purpose |
|---|---|---|
| JDK | Java Development Kit | Used to develop and run Java programs |
| JRE | Java Runtime Environment | Provides the environment to run Java programs |
| JVM | Java Virtual Machine | Executes Java bytecode |

**JDK:**

JDK provides tools required to develop Java applications, including the Java compiler.

**JRE:**

JRE provides the libraries and runtime environment needed to run Java applications.

**JVM:**

JVM executes Java bytecode and helps make Java platform independent.

**Remember:**

- JDK = Development tools + runtime components.
- JRE = Runtime environment.
- JVM = Executes bytecode.

**Follow-up Questions:**

- What is the Java compiler?
- What is bytecode?
- Is JVM platform independent?
- What happens after compilation?

---

### 3. What Are the Four Pillars of OOP?

OOP stands for Object-Oriented Programming.

The four main pillars are:

#### 1. Encapsulation

Encapsulation means wrapping data and methods together in a class and controlling access to the data.

**Example:**

```java
class Student {
    private int age;

    public void setAge(int age) {
        this.age = age;
    }

    public int getAge() {
        return age;
    }
}
```

Here, `private` protects the variable, while getter and setter methods provide controlled access.

#### 2. Inheritance

Inheritance allows one class to acquire properties and methods from another class.

**Example:**

```java
class Animal {
    void eat() {
        System.out.println("Eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking");
    }
}
```

Here, Dog inherits from Animal using `extends`.

#### 3. Polymorphism

Polymorphism means one name or interface can represent different behaviours.

Two common types:

- Compile-time polymorphism – Method overloading.
- Runtime polymorphism – Method overriding.

#### 4. Abstraction

Abstraction means hiding implementation details and showing essential functionality.

**Example:**

```java
abstract class Vehicle {
    abstract void start();
}

class Car extends Vehicle {
    void start() {
        System.out.println("Car starts");
    }
}
```

**Follow-up Questions:**

- What is the difference between abstraction and encapsulation?
- What is inheritance?
- What are the types of polymorphism?
- Can Java support multiple inheritance through classes?

---

### 4. Difference Between Class and Object

**Class:**

A class is a blueprint or template used to create objects.

**Object:**

An object is an instance of a class.

**Example:**

```java
class Student {
    String name = "Imran";

    void study() {
        System.out.println("Student is studying");
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();

        System.out.println(s1.name);
        s1.study();
    }
}
```

**Explanation:**

- `Student` is the class.
- `s1` is a reference variable.
- `new Student()` creates an object.
- `name` is an instance variable.
- `study()` is a method.

**Follow-up Questions:**

- What is an instance?
- What is the `new` keyword?
- Where are Java objects generally stored?
- Can we create multiple objects from one class?

---

### 5. Difference Between Method Overloading and Method Overriding

#### Method Overloading

Method overloading means defining multiple methods with the same name but different parameter lists in the same class.

**Example:**

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

#### Method Overriding

Method overriding occurs when a subclass provides its own implementation of an inherited method.

**Example:**

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}
```

**Difference:**

| Overloading | Overriding |
|---|---|
| Same method name | Same method signature |
| Different parameters | Same parameters |
| Usually within the same class | Requires inheritance |
| Compile-time polymorphism | Runtime polymorphism |

**Follow-up Questions:**

- Can we overload the main method?
- Can we override a static method?
- Can we override a final method?
- What is the `@Override` annotation?

---

### 6. What Is a Constructor in Java?

A constructor is a special member of a class used to initialize an object.

**Important Features:**

- Constructor name must match the class name.
- It does not have a return type.
- It is called when an object is created.
- Constructors can be overloaded.
- Constructors are not inherited.

**Types of Constructors:**

1. Default constructor – Provided
