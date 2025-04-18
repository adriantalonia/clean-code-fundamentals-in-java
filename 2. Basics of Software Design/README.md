# 2 Basics of Software Design

## 📋 Table of Contents
- [2 Basics of Software Design](#2-basics-of-software-design)
  - [📋 Table of Contents](#-table-of-contents)
  - [📐 2.1 Software Design Pyramid](#-21-software-design-pyramid)
    - [🔷 1. Basic Concepts of Object-Oriented Design (OOD)](#-1-basic-concepts-of-object-oriented-design-ood)
      - [Key Concepts:](#key-concepts)
    - [💡 2. Design Principles](#-2-design-principles)
      - [Common Principles (SOLID):](#common-principles-solid)
    - [🎯 3. Design Patterns](#-3-design-patterns)
      - [Examples:](#examples)
    - [🏛️ 4. Architecture Patterns](#️-4-architecture-patterns)
      - [Examples:](#examples-1)
    - [🧠 Summary Table](#-summary-table)
    - [❓ Interview Questions](#-interview-questions)
- [2.2 Basic Concepts of OOD (Object-Oriented Design)](#22-basic-concepts-of-ood-object-oriented-design)
  - [Class and Object](#class-and-object)
    - [Definition](#definition)
    - [Purpose](#purpose)
    - [Example in Java:](#example-in-java)
  - [🔑 Key OOD Concepts](#-key-ood-concepts)
    - [1. **Abstraction**](#1-abstraction)
      - [Abstract Class vs Interface in Java](#abstract-class-vs-interface-in-java)
      - [Best practices for abstract classes in Java:](#best-practices-for-abstract-classes-in-java)
      - [🎯 When to Choose Abstract Classes Over Interfaces](#-when-to-choose-abstract-classes-over-interfaces)
      - [Best practices for interfaces in Java:](#best-practices-for-interfaces-in-java)
      - [🎯 When to Choose Interfaces Over Abstract Classes](#-when-to-choose-interfaces-over-abstract-classes)
    - [2. **Encapsulation**](#2-encapsulation)
    - [3. **Inheritance**](#3-inheritance)
    - [4. **Polymorphism**](#4-polymorphism)
      - [🔸 1. Compile-Time Polymorphism (Method Overloading)](#-1-compile-time-polymorphism-method-overloading)
      - [🔸 2. Runtime Polymorphism (Method Overriding)](#-2-runtime-polymorphism-method-overriding)
      - [🔄 Polymorphism and Interfaces](#-polymorphism-and-interfaces)
      - [🧠 Summary Table](#-summary-table-1)
  - [🎯 Summary Table](#-summary-table-2)
  - [❓ Interview Questions (with sample answers)](#-interview-questions-with-sample-answers)
  


## 📐 2.1 Software Design Pyramid

![image](resources/images/Software-Design-Pyramid.png)

The Software Design Pyramid is a conceptual model that structures the evolution of software design skills and practices into four progressive layers. Each layer builds upon the foundations established in the one below it, guiding developers toward mastering software craftsmanship.


---

### 🔷 1. Basic Concepts of Object-Oriented Design (OOD)

This is the foundation of the pyramid and includes key ideas that every developer must master to write structured and maintainable code.

#### Key Concepts:
- **Class and Object**: Core units of object-oriented programming.
- **Encapsulation**: Bundling data with methods that operate on that data.
- **Abstraction**: Hiding complexity and showing only essential features.
- **Inheritance**: Mechanism to derive new classes from existing ones.
- **Polymorphism**: Ability to call the same method on different objects and have each respond in its own way.

---

### 💡 2. Design Principles

Design principles help improve the structure and maintainability of codebases. They act as guidelines to write better object-oriented code.

#### Common Principles (SOLID):
- **S** - Single Responsibility Principle
- **O** - Open/Closed Principle
- **L** - Liskov Substitution Principle
- **I** - Interface Segregation Principle
- **D** - Dependency Inversion Principle

These principles promote scalability, flexibility, and testability.

---

### 🎯 3. Design Patterns

Design patterns are general, reusable solutions to commonly occurring problems in software design. They are based on design principles.

#### Examples:
- **Creational**: Singleton, Factory, Builder
- **Structural**: Adapter, Decorator, Composite
- **Behavioral**: Observer, Strategy, Command

---

### 🏛️ 4. Architecture Patterns

Architecture patterns define the overall structure of applications and how different modules communicate.

#### Examples:
- **Layered Architecture**
- **Microservices Architecture**
- **Event-Driven Architecture**
- **Hexagonal Architecture**

These patterns help manage complexity at a system-wide level and support maintainability and scalability.

---

### 🧠 Summary Table

| Layer                     | Focus Area                    | Goal                                 |
| ------------------------- | ----------------------------- | ------------------------------------ |
| **Architecture Patterns** | System-wide structure         | Scalability and maintainability      |
| **Design Patterns**       | Code-level reusable solutions | Reusability and flexibility          |
| **Design Principles**     | Guidelines for code structure | Clean and maintainable object design |
| **Basic concepts of OOD** | Core OOP ideas                | Foundational programming knowledge   |

### ❓ Interview Questions

1. **What are the four layers of the Software Design Pyramid?**  
   > The layers are: Basic Concepts of OOD, Design Principles, Design Patterns, and Architecture Patterns.

2. **Why is object-oriented design fundamental to this pyramid?**  
   > It provides the building blocks (classes, objects, polymorphism) for all higher-level design practices citeturn1view0.

3. **How do SOLID principles contribute to maintainability?**  
   > They enforce single responsibility, open/closed extension, substitutability, interface segregation, and dependency inversion for flexible and robust code citeturn2view0.

4. **Give an example of how a design pattern and an architecture pattern differ.**  
   > A Factory Method (design pattern) creates objects, while Layered Architecture (architecture pattern) separates application concerns across layers citeturn3view0 citeturn0search3.

5. **Why might a team choose Event-Driven Architecture?**  
   > For decoupled communication, scalability, and real-time processing needs citeturn0search8.

---
---


# 2.2 Basic Concepts of OOD (Object-Oriented Design)

![image](resources/images/ODD.png)

This section introduces the four fundamental principles of Object-Oriented Design (OOD), which form the backbone of designing clean and modular software in Java.

---

## Class and Object

### Definition
- A **class** is a blueprint or template for creating objects. It defines properties (fields) and behaviors (methods) that its instances (objects) will have.
- An **object** is an instance of a class, representing a specific entity with actual values stored in memory.

### Purpose
- Classes allow for code reuse, structure, and abstraction by defining types of entities.
- Objects encapsulate data and behavior, enabling modular, maintainable, and testable programs.

### Example in Java:
```java
// Class definition
public class Car {
    String color;
    String model;

    void drive() {
        System.out.println("The car is driving.");
    }
}

// Creating objects from the class
public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.color = "Red";
        myCar.model = "Toyota Corolla";
        myCar.drive(); // Output: The car is driving.
    }
}
```


## 🔑 Key OOD Concepts

### 1. **Abstraction**

**Definition:**  

**Abstraction** is the process of hiding unnecessary internal implementation details and exposing only the essential characteristics and behavior of an object.

It allows you to define **what** an object does, rather than **how** it does it.

In Java, abstraction is achieved in two primary ways:
- **Abstract classes**
- **Interfaces**

**Purpose:**  
- Simplifies complex systems by focusing only on relevant details.
- Promotes loose coupling between components.
- Facilitates code readability and maintenance.
- Enables flexibility and extensibility in design.

Abstraction plays a crucial role in API design, system architecture, and component interaction. It allows developers to use functionality without needing to understand or modify the underlying implementation.

**🏗️ Real-World Analogy**

Think of **a car**:
- **You use it** by pressing pedals, turning the wheel, etc. (**what** it does).
- You **don’t need to know** how the fuel injection system or engine management works (**how** it does it).



**💡 Java Example: Abstract Class**
```java
// Abstract class
// 1. Abstract class definition
// - Serves as a base template for all animals
// - Cannot be instantiated directly (can't do 'new Animal()')
abstract class Animal {
    // 2. Abstract method (no implementation)
    // - Forces all concrete subclasses to provide their own implementation
    // - Defines WHAT animals must do (make sound), not HOW
    abstract void makeSound();
    
    // 3. Concrete method with implementation
    // - Shared behavior for ALL animal subclasses
    // - Subclasses inherit this automatically (can optionally override)
    void sleep() {
        System.out.println("Sleeping...");
    }
}

// 4. Concrete subclass
// - Provides specific implementation of the abstract method
class Dog extends Animal {
    @Override
    void makeSound() {
        // Dog-specific sound implementation
        System.out.println("Woof!");
        // Could add dog-specific logic here
    }
    
    // Note: sleep() is inherited but NOT overridden
    // Dogs use the default animal sleeping behavior
}

public class Main {
    public static void main(String[] args) {
        // 5. Polymorphism in action
        // - Variable declared as Animal type (abstract)
        // - Actually holds a Dog instance (concrete)
        Animal myDog = new Dog();
        
        // 6. Method calls demonstrate:
        // - makeSound() uses Dog's implementation
        myDog.makeSound(); // Output: "Woof!"
        
        // - sleep() uses inherited Animal implementation
        myDog.sleep();     // Output: "Sleeping..."
        
        // 7. Why this matters:
        // - We could create other animals easily:
        //   class Cat extends Animal { ... }
        // - All would share sleep() behavior
        // - Each would implement makeSound() differently
    }
}
```

**💡 Java Example: Interface**
```java
// 1. Define the abstraction (contract)
// The interface declares WHAT payment methods must do, not HOW they do it
interface PaymentMethod {
    // Any class implementing this interface MUST provide this method
    void pay(double amount);
}

// 2. Concrete implementation #1
class CreditCard implements PaymentMethod {
    @Override
    public void pay(double amount) {
        // Actual implementation for credit card payments
        System.out.println("Paid $" + amount + " with Credit Card.");
        // In a real app, this would connect to a payment gateway
    }
}

// 3. Concrete implementation #2 
class PayPal implements PaymentMethod {
    @Override
    public void pay(double amount) {
        // Different implementation for PayPal
        System.out.println("Paid $" + amount + " with PayPal.");
        // Would actually call PayPal's API here
    }
}

public class Checkout {
    public static void main(String[] args) {
        // 4. Polymorphism in action
        // We declare the variable as the INTERFACE type
        PaymentMethod method;
        
        // But instantiate a CONCRETE implementation
        method = new PayPal();  // Could easily swap to CreditCard here
        
        // 5. The magic of abstraction:
        // - Checkout class ONLY knows about the PaymentMethod interface
        // - It doesn't care which concrete implementation is used
        method.pay(50.0); 
        
        // 6. Key benefits:
        // - Easy to add new payment methods (just implement the interface)
        // - No changes needed in Checkout when adding new methods
        // - Loose coupling between components
    }
}
```

#### Abstract Class vs Interface in Java

**Comparison Table** 📊 

| Feature            | Abstract Class                                | Interface                                                                       |
| ------------------ | --------------------------------------------- | ------------------------------------------------------------------------------- |
| **Purpose**        | Partial abstraction, shared implementation    | Complete abstraction, contract                                                  |
| **Methods**        | Can have abstract and non-abstract methods    | Traditionally only abstract methods (default/static methods allowed in Java 8+) |
| **Inheritance**    | Supports single inheritance                   | Supports multiple inheritance                                                   |
| **Variables**      | Can have static, non-static, final, non-final | Only `static final` variables                                                   |
| **Implementation** | Subclass must implement all abstract methods  | Implementing class must provide all method implementations                      |
| **Instantiation**  | Cannot be instantiated directly               | Cannot be instantiated directly                                                 |
| **Constructors**   | Can have constructors                         | Cannot have constructors                                                        |
| **Main method**    | Can have a `main` method                      | Cannot have a `main` method                                                     |

---

**🎯 When to Use**

 **Abstract Classes**
- ✅ When you need to **share common implementation** among subclasses.
- ✅ When you want to **enforce a class hierarchy** (e.g., base class with partial defaults).
- ✅ When you need **constructors** or **non-final variables**.

 **Interfaces**
- ✅ When you need **multiple inheritance** of behavior (Java 8+ supports default methods).
- ✅ When defining a **contract** (e.g., APIs, callbacks).
- ✅ When you want **loose coupling** ("program to interfaces, not implementations").


#### Best practices for abstract classes in Java:

**1. Sharing Common Implementation**
```java
abstract class Animal {
    // Concrete method (shared by all subclasses)
    public void eat() {
        System.out.println("This animal eats food.");
    }

    // Abstract method (must be implemented by subclasses)
    public abstract void makeSound();
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.eat();       // Inherited from Animal (shared implementation)
        myDog.makeSound();  // Dog-specific implementation
    }
}
```

**Key Points:**

- Animal provides reusable **eat**() method.
- Subclasses must implement **makeSound**().


**2. Enforcing Hierarchy with Defaults**

```java
abstract class Shape {
    protected String color;  // Non-final field

    // Abstract class CAN have constructors
    public Shape(String color) {
        this.color = color;
    }

    // Concrete method
    public String getColor() {
        return color;
    }

    // Abstract method (enforces implementation)
    public abstract double area();
}

class Circle extends Shape {
    private double radius;

    public Circle(String color, double radius) {
        super(color);  // Calls parent constructor
        this.radius = radius;
    }

    @Override
    public double area() {
        return Math.PI * radius * radius;
    }
}

public class Main {
    public static void main(String[] args) {
        Circle myCircle = new Circle("Red", 5.0);
        System.out.println("Color: " + myCircle.getColor());  // From Shape
        System.out.println("Area: " + myCircle.area());      // Circle's implementation
    }
}
```

**Key Points:**

- Shape enforces area() calculation for all shapes.
- Constructor initializes shared state (color).


**3. Using Constructors and Non-Final Fields**
```java
abstract class Vehicle {
    protected String model;  // Mutable field (non-final)
    protected int year;

    // Constructor in abstract class
    public Vehicle(String model, int year) {
        this.model = model;
        this.year = year;
    }

    // Concrete method
    public void startEngine() {
        System.out.println(model + "'s engine started.");
    }

    // Abstract method
    public abstract void stopEngine();
}

class Car extends Vehicle {
    public Car(String model, int year) {
        super(model, year);
    }

    @Override
    public void stopEngine() {
        System.out.println(model + "'s engine stopped.");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("Tesla Model 3", 2023);
        myCar.startEngine();  // Inherited from Vehicle
        myCar.stopEngine();   // Car-specific implementation
    }
}
```

**Key Points:**

- Vehicle manages common fields (model, year).
- Subclasses extend behavior while reusing base logic.

#### 🎯 When to Choose Abstract Classes Over Interfaces


| Scenario                     | Abstract Class | Interface                |
| ---------------------------- | -------------- | ------------------------ |
| Share method implementations | ✅ Yes          | ❌ No (pre-Java 8)        |
| Use constructors             | ✅ Yes          | ❌ No                     |
| Non-final fields             | ✅ Yes          | ❌ No (only static final) |
| Single inheritance           | ✅ Yes          | ❌ No (multiple allowed)  |

💡 Java 8+ Note: Interfaces can now have default methods, but still lack constructors and mutable fields.



#### Best practices for interfaces in Java:

**1: Multiple Inheritance of Behavior**

```java
// Interface defining flying capability
interface Flyable {
    // Java 8+ default method (shared behavior)
    default void takeOff() {
        System.out.println("Default takeoff procedure");
    }
    
    // Traditional abstract method
    void fly();
}

// Interface defining swimming capability
interface Swimmable {
    default void startSwimming() {
        System.out.println("Entering the water");
    }
    
    void swim();
}

// Class can implement MULTIPLE interfaces (Java doesn't allow multiple class inheritance)
class Duck implements Flyable, Swimmable {
    @Override
    public void fly() {
        System.out.println("Duck flying with wings");
    }
    
    @Override
    public void swim() {
        System.out.println("Duck paddling in water");
    }
    
    // Can override default methods if needed
    @Override
    public void takeOff() {
        System.out.println("Duck running on water to take off");
    }
}

public class Main {
    public static void main(String[] args) {
        // 1. Multiple inheritance demonstration
        Duck donald = new Duck();
        donald.takeOff();  // Uses overridden default method
        donald.fly();
        donald.startSwimming();  // Uses default method from Swimmable
        donald.swim();
    }
}
```

**Key Points:**

**✅ Core Advantage:**

- Classes can implement multiple interfaces (unlike single inheritance with abstract classes).

**🛠 Java 8+ Features:**

- default methods enable shared behavior in interfaces (e.g., Flyable.takeOff()).
- Subclasses can override default methods or use them as-is.

**⚠ Limitations:**

- No instance fields (only static final constants).
- No constructors.


**2: Defining Contracts (APIs)**

```java
// Payment processing contract
interface PaymentProcessor {
    // No implementation details - pure contract
    void processPayment(double amount);
    boolean validatePayment();
}

// Concrete implementation for Stripe
class StripeProcessor implements PaymentProcessor {
    @Override
    public void processPayment(double amount) {
        System.out.println("Processing $" + amount + " via Stripe");
        // Actual Stripe API calls would go here
    }
    
    @Override
    public boolean validatePayment() {
        System.out.println("Stripe validation complete");
        return true;
    }
}

public class Main {
    public static void main(String[] args) {
        // 2. Contract/API usage
        PaymentProcessor stripe = new StripeProcessor();
        stripe.processPayment(99.99);

    }
}
```

**Key Points:**

**✅ Core Advantage:**

- Enforces "what" (method signatures) without specifying "how".

**📜 Standard Uses:**

- API design (e.g., PaymentProcessor).
- Callback systems (e.g., EventListener).

**⚡ Critical Note:**

- All interface methods are implicitly public abstract (except default/static).


**Scenario 3: Loose Coupling**

```java
// High-level module depends on abstraction
class OrderService {
    private PaymentProcessor processor;
    
    // Constructor injection (dependency inversion)
    public OrderService(PaymentProcessor processor) {
        this.processor = processor;
    }
    
    public void checkout(double amount) {
        if (processor.validatePayment()) {
            processor.processPayment(amount);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        PaymentProcessor stripe = new StripeProcessor();
        stripe.processPayment(99.99);
        // 3. Loose coupling in action
        OrderService service = new OrderService(stripe);
        service.checkout(49.95);
        // Could easily switch payment providers without changing OrderService:
        // OrderService paypalService = new OrderService(new PayPalProcessor());
    }
}

```

**Key Points:**

**✅ Core Advantage:**

- Depend on abstractions (interfaces), not concrete implementations.

**📌 SOLID Principle:**

- Dependency Inversion (D in SOLID): High-level modules shouldn’t depend on low-level details.

**🔄 Flexibility:**

- Easily swap implementations (e.g., OrderService using StripeProcessor or PayPalProcessor).


#### 🎯 When to Choose Interfaces Over Abstract Classes


| Scenario               | Interface                                    | Abstract Class                            |
| ---------------------- | -------------------------------------------- | ----------------------------------------- |
| Multiple inheritance   | ✅ Yes (unlimited implementations)            | ❌ No (single inheritance only)            |
| API contracts          | ✅ Perfect for pure abstractions              | ⚠️ Less ideal (can contain implementation) |
| Default methods        | ✅ Yes (Java 8+)                              | ❌ N/A (all methods can have bodies)       |
| Loose coupling         | ✅ Ideal ("program to interfaces")            | ⚠️ Tighter coupling to hierarchy           |
| Functional programming | ✅ Single-method interfaces work with lambdas | ❌ Not applicable                          |
| State management       | ❌ No fields (except static final)            | ✅ Can have instance fields                |
| Constructors           | ❌ Never                                      | ✅ Yes                                     |
| Code reuse             | ⚠️ Limited (default methods only)             | ✅ Full shared implementations             |


---
---

### 2. **Encapsulation**

**Definition:**  

**Encapsulation** is an object-oriented programming principle that combines data (fields) and behavior (methods) within a single unit — a class — and restricts direct access to the internal representation of the object.

**It ensures that:**

- The internal state of an object is hidden from the outside.
- All interaction with the object happens through a controlled interface.

**This is typically done using:**

- `private` fields (data hiding)
- `public` getter and setter methods

**Purpose:**  
- Protects internal state.
- Reduces coupling.
- **Protects data integrity** by preventing unauthorized or unintended access.
- **Enforces control** over how data is accessed or modified.
- **Supports refactoring** and maintenance by isolating implementation.
- **Improves modularity** and encourages cleaner APIs.

> Encapsulation encourages developers to design systems as **black boxes** where internal changes don’t affect external behavior, as long as the interface remains the same.

**🏗️ Real-World Analogy**

Think of **a vending machine**:
- You interact with it through buttons and money slots (public interface).
- You **cannot access** or manipulate the internal wiring or item storage (private state).
- All actions go through **well-defined operations**.


**💡 Java Example: Using Private Fields and Accessors**

```java
public class BankAccount {
    private double balance; // private field

    public double getBalance() {
        return balance;
    }

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    public boolean withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            return true;
        }
        return false;
    }
}
```

**Explanation:**

- The balance field is hidden (private) and cannot be accessed directly from outside.
- Access is provided through the getBalance(), deposit(), and withdraw() methods.
- This prevents illegal operations like setting a negative balance directly.

✅ Benefits of Encapsulation

| Benefit           | Description                                                     |
| ----------------- | --------------------------------------------------------------- |
| Data Protection   | Prevents unauthorized changes to internal state.                |
| Controlled Access | Logic can be added to validate or transform values.             |
| Modularity        | Class internals can change without affecting external code.     |
| Reusability       | Well-encapsulated classes are more reusable and easier to test. |


**🛠️ Best Practices**
- Always keep class fields **private** or **protected**.
- Expose only necessary behavior via **public methods**.
- Avoid exposing **internal mutable** objects directly.
- Consider immutability when possible (**no setters**).

**🗣️ Interview Tip**
 > "Encapsulation is not just about data hiding, but about behavior control and interface design. It ensures that objects have well-defined boundaries and interactions."

---
---

### 3. **Inheritance**

**Definition:**  

**Inheritance** is an object-oriented programming principle where a new class (called a **subclass** or **child class**) is derived from an existing class (called a **superclass** or **parent class**).

The subclass **inherits** attributes (fields) and behaviors (methods) from the superclass, allowing for code reuse and the creation of hierarchical relationships between classes.

Java supports **single inheritance** — a class can inherit from only one parent class but can implement multiple interfaces.


**Purpose:**  
- **Code Reusability**: Common functionality is written once in the parent class and reused in child classes.
- **Logical Hierarchy**: Represents real-world relationships (e.g., a Dog is an Animal).
- **Extensibility**: Child classes can extend or override parent behavior as needed.
- **Maintainability**: Centralizes shared logic for easier updates.

**🏗️ Real-World Analogy**

Think of **a general Animal** class:
- All animals eat and sleep (shared behavior).
- A **Dog** is a type of **Animal**, but it also barks (specialized behavior).

> Instead of rewriting eat/sleep for every animal, you write them once in the `Animal` class.


**Example in Java:**

```java
// Superclass
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

// Subclass
class Dog extends Animal {
    void bark() {
        System.out.println("Woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();  // Inherited from Animal
        dog.bark(); // Defined in Dog
    }
}
```

**Explanation:**

- Dog inherits the eat() method from Animal.
- It also adds its own method: bark().


**🔁 Method Overriding**

Subclasses can modify the behavior of methods inherited from the parent class by overriding them.

```java
class Animal {
    void makeSound() {
        System.out.println("Some generic animal sound");
    }
}

class Cat extends Animal {
    @Override
    void makeSound() {
        System.out.println("Meow!");
    }
}

```

- **@Override** tells the compiler we're intentionally replacing the parent method.
- **Polymorphism** works with **inheritance** (see next section on Polymorphism).

**🚫 When Not to Use Inheritance**
Inheritance is powerful but can be misused:

- If classes do not share a true "is-a" relationship.
- If adding inheritance makes classes tightly coupled.
- When composition would provide better flexibility.


✅ Favor Composition Over Inheritance (When Appropriate)

```java
// Instead of Dog extends Animal,
// Use Dog has an AnimalBehavior:

class AnimalBehavior {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog {
    private AnimalBehavior behavior = new AnimalBehavior();

    void eat() {
        behavior.eat();
    }

    void bark() {
        System.out.println("Woof!");
    }
}

```

- Composition allows combining behaviors from multiple sources.
- Promotes looser coupling and greater flexibility.

**📌 Key Terms**

| Term       | Description                                  |
| ---------- | -------------------------------------------- |
| Superclass | The base class being inherited from          |
| Subclass   | The class that inherits from the superclass  |
| extends    | Java keyword used for class inheritance      |
| Overriding | Redefining inherited methods in the subclass |
| super      | Refers to the parent class and its members   |


**🧠 Summary**

| Feature         | Description                        |
| --------------- | ---------------------------------- |
| Code Reuse      | Share functionality across classes |
| Hierarchy       | Models real-world relationships    |
| Flexibility     | Override behavior in subclasses    |
| Maintainability | Centralized updates and fixes      |


**🛠️ Best Practices**

- Ensure a true "is-a" relationship exists before using inheritance.
- Prefer composition when relationships are "has-a" or "uses-a".
- Use @Override annotations to avoid accidental method mismatches.
- Avoid deep inheritance trees — they are hard to manage and test.
- Keep superclass design stable and consistent.

**❓ Interview Tip**
> “Inheritance models an is-a relationship. Use it when one class is a specialized version of another — not just because they happen to share code.”

---
---

### 4. **Polymorphism**

**Definition:**  

**Polymorphism** is an object-oriented programming principle that allows a single interface or method to operate on objects of different types.

The term "polymorphism" means **“many forms”** — the same operation behaves differently depending on the context, making systems more flexible and extensible.

In Java, there are **two types of polymorphism**:
1. **Compile-time Polymorphism** (Static Binding) — achieved through method overloading.  
2. **Runtime Polymorphism** (Dynamic Binding) — achieved through method overriding and inheritance.


**Purpose:**  
- **Extensibility**: Easily add new behavior with minimal changes to existing code.
- **Maintainability**: Reduce code duplication by treating different objects uniformly.
- **Reusability**: Write generic methods or components that work across multiple types.
- **Decoupling**: Isolate the logic that depends on behavior, not concrete types.

**🏗️ Real-World Analogy**

Think of a **remote control**:

- The same "power" button works on TVs, projectors, and sound systems.
- The action (turning on/off) is context-specific, but the interface (button) remains the same.


#### 🔸 1. Compile-Time Polymorphism (Method Overloading)

Occurs when multiple methods in the same class have the same name but different parameters (signature).

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

> Note: The correct method is chosen at compile time based on the arguments provided.


#### 🔸 2. Runtime Polymorphism (Method Overriding)

Occurs when a subclass provides a specific implementation of a method already defined in its superclass.


**Example in Java:**
```java
class Animal {
    void makeSound() {
        System.out.println("Some animal sound");
    }
}

class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Woof!");
    }
}

class Cat extends Animal {
    @Override
    void makeSound() {
        System.out.println("Meow!");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a1 = new Dog();
        Animal a2 = new Cat();

        a1.makeSound(); // Woof!
        a2.makeSound(); // Meow!
    }
}
```

> Note: The method to call is determined at runtime, depending on the object type.


#### 🔄 Polymorphism and Interfaces
Polymorphism shines when used with interfaces. This allows different implementations to be used interchangeably.

```java
interface Shape {
    void draw();
}

class Circle implements Shape {
    public void draw() {
        System.out.println("Drawing a circle");
    }
}

class Square implements Shape {
    public void draw() {
        System.out.println("Drawing a square");
    }
}

public class DrawingTool {
    public static void main(String[] args) {
        Shape shape1 = new Circle();
        Shape shape2 = new Square();

        shape1.draw(); // Drawing a circle
        shape2.draw(); // Drawing a square
    }
}
```

#### 🧠 Summary Table

| Type of Polymorphism       | How it works                                 | When it's resolved | Example                              |
| -------------------------- | -------------------------------------------- | ------------------ | ------------------------------------ |
| Compile-time (Overloading) | Method name + different params               | At compile time    | add(int, int) vs add(double, double) |
| Runtime (Overriding)       | Subclass redefines superclass method         | At runtime         | makeSound() in Dog vs Cat            |
| Interface-based            | Different classes implement common interface | At runtime         | draw() in Circle and Square          |


**✅ Best Practices**
- Use polymorphism to write generic and reusable code.
- Program to interfaces, not concrete implementations.
- Avoid type-checking (instanceof) — let polymorphism handle behavior.
- Use method overriding with @Override for clarity and safety.

**🚫 Common Mistakes**
- Confusing overloading with overriding.
- Violating the Liskov Substitution Principle (L in SOLID) by breaking expected behavior.
- Adding redundant methods that reduce polymorphic usefulness.

**🗣️ Interview Tip**

“Polymorphism allows you to treat different types uniformly through a shared interface, enabling extensible and elegant code design. It's a cornerstone of scalable OOP systems.”


---
---

## 🎯 Summary Table

| Concept       | Purpose                   | Real-world Example                                              |
| ------------- | ------------------------- | --------------------------------------------------------------- |
| Abstraction   | Hide complexity           | TV remote controls TV functions without exposing inner workings |
| Encapsulation | Hide internal state       | Private fields in classes                                       |
| Inheritance   | Reuse existing behavior   | Dog is-an Animal                                                |
| Polymorphism  | Many forms, one interface | draw() method for different shapes                              |

---

## ❓ Interview Questions (with sample answers)

1. **What is the difference between abstraction and encapsulation?**  
   > Abstraction hides complexity by providing a simplified interface. Encapsulation hides the internal state and enforces access via methods.

2. **Can Java support multiple inheritance?**  
   > Java supports multiple inheritance through interfaces, not classes.

3. **Why is polymorphism important in OOP?**  
   > It allows objects to be treated as instances of their parent type, enabling dynamic method resolution and flexible code design.

4. **Give a real-world analogy for encapsulation.**  
   > A capsule pill — it hides the medicine inside and you only see the outer shell.

5. **How does method overloading differ from overriding?**  
   > Overloading is compile-time polymorphism (same method name, different parameters), while overriding is runtime polymorphism (same method signature in subclass).

---

Mastering these OOD principles is crucial for writing maintainable and scalable Java applications.