---
title: Introduction to GitHub Actions for Beginners
author: John Ng
date: "2024-05-01"
theme: seriph
---
# Introduction to Object-Oriented Programming in C#

---

## Agenda

1. **What is Object-Oriented Programming (OOP)?**
2. **Core Concepts of OOP:**
   - Classes and Objects
   - Encapsulation
   - Inheritance
   - Polymorphism
   - Abstraction
3. **OOP in C# Examples**
4. **Summary and Q&A**

---

## What is Object-Oriented Programming?

- **Definition:** A programming paradigm based on the concept of "objects" which can contain data and methods.
- **Purpose:** To design software by modeling real-world entities.
- **Benefits:**
  - Modularity
  - Reusability
  - Flexibility
  - Maintainability

---

<div style="display: flex; justify-content: center; align-items: center; height: 100%;">
  <h1>Classes and Objects</h1>
</div>

---

### **Classes**

- A blueprint for creating objects.
- Defines properties (attributes) and methods (behaviors).

```csharp
public class Person
{
    // Properties
    public string Name { get; set; }
    public int Age { get; set; }
    
    // Method
    public void Introduce()
    {
        Console.WriteLine($"Hi, I'm {Name} and I'm {Age} years old.");
    }
}
```
---

### **Objects**

- Instances of classes.
- Created using the `new` keyword.

```csharp
Person person = new Person();
person.Name = "Alice";
person.Age = 30;
person.Introduce();
```

---

## Encapsulation

- **Definition:** Wrapping data and methods that operate on data within one unit (class).
- **Access Modifiers:**
  - `public` – Accessible from anywhere.
  - `private` – Accessible only within the class.
  - `protected` – Accessible within the class and derived classes.

---

### Encapsulation **Example:**

```csharp
public class BankAccount
{
    // Private field
    private decimal balance;
    
    // Public method to access private field
    public void Deposit(decimal amount)
    {
        if (amount > 0)
            balance += amount;
    }
    
    public decimal GetBalance()
    {
        return balance;
    }
}
```

---

## Inheritance

- **Definition:** A mechanism where a new class derives from an existing class.
- **Base Class (Parent)**
- **Derived Class (Child)**

---

### Inheritance **Example:**

```csharp
// Base class
public class Animal
{
    public void Eat()
    {
        Console.WriteLine("Eating...");
    }
}

// Derived class
public class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Barking...");
    }
}
```

```csharp
Dog dog = new Dog();
dog.Eat();  // Inherited method
dog.Bark(); // Own method
```

---

## Polymorphism

- **Definition:** Ability of objects to take on many forms.
- **Types:**
  - **Compile-time (Method Overloading)**
  - **Run-time (Method Overriding)**

---

### **Method Overloading (Compile-time)**

```csharp
public class Calculator
{
    public int Add(int a, int b) { return a + b; }
    public double Add(double a, double b) { return a + b; }
}
```

### **Method Overriding (Run-time)**

```csharp
public class Animal
{
    public virtual void Speak()
    {
        Console.WriteLine("Animal sound");
    }
}

public class Cat : Animal
{
    public override void Speak()
    {
        Console.WriteLine("Meow");
    }
}
```

---

## Abstraction

- **Definition:** Hiding complex implementation details and showing only the necessary features.

### **Abstract Classes**

- Cannot be instantiated.
- Can have abstract and non-abstract members.

```csharp
public abstract class Shape
{
    public abstract double GetArea();
}
```

### **Derived Class Implementation**

```csharp
public class Rectangle : Shape
{
    public double Width { get; set; }
    public double Height { get; set; }
    
    public override double GetArea()
    {
        return Width * Height;
    }
}
```

---

## Interfaces

- **Definition:** A contract that defines a set of methods and properties without implementation.
- **Purpose:** To achieve multiple inheritances and loose coupling.

### **Example Interface:**

```csharp
public interface IMovable
{
    void Move();
}
```

### **Implementing Interface:**

```csharp
public class Car : IMovable
{
    public void Move()
    {
        Console.WriteLine("The car is moving.");
    }
}
```

---

## OOP in C# Examples

### **Combining Concepts**

```csharp
public abstract class Employee
{
    public string Name { get; set; }
    public abstract void Work();
}

public class Developer : Employee
{
    public override void Work()
    {
        Console.WriteLine($"{Name} is writing code.");
    }
}

public class Manager : Employee
{
    public override void Work()
    {
        Console.WriteLine($"{Name} is managing the team.");
    }
}
```

---

## Summary

- **OOP Principles:**
  - **Encapsulation:** Protecting data through access modifiers.
  - **Inheritance:** Deriving new classes from existing ones.
  - **Polymorphism:** Interacting with objects through a common interface.
  - **Abstraction:** Simplifying complex reality using models.

- **Advantages of OOP:**
  - Improved software maintainability.
  - Easier troubleshooting and code reusability.
  - Real-world modeling.

---

## Q&A

<div style="display: flex; justify-content: center; align-items: center; height: 100%;">
  <h1>Questions?</h1>
</div>

---