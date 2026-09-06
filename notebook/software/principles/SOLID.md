# SOLID Design Principles  

**SOLID** is a set of five **Object-Oriented Design** principles that can help make software easier to understand, maintain, test, and extend.  

```
S – Single Responsibility Principle  
O – Open-Closed Principle  
L – Liskov Substitution Principle  
I – Interface Segregation Principle  
D – Dependency Inversion Principle  
```

> [!WARNING]  
> These principles serve as guidelines rather than strict rules. Blindly applying all of them can lead to unnecessary abstraction, indirection, and complexity. Instead, they should be applied with discretion and weighed against the costs they introduce.

## S - Single Responsibility Principle (SRP)  

> **A class should have one reason to change.**  

A class should have a focused responsibility so that changes to one responsibility do not unnecessarily affect unrelated behavior.  
  

## O - Open-Closed Principle (OCP)  

> **Open for extension, but closed for modification.**  

New behavior should ideally be added without changing stable, existing code.  
Can often be achieved through abstractions, polymorphism, composition, or patterns like Strategy.
  
  
## L- Liskov Substitution Principle (LSP)  

> **A subtype should be usable wherever its parent type is expected, without breaking the expected behavior.**  

In simple terms:  

If replace the parent with the child, the code should still work as expected.  
A subtype should follow the behavior and expectations defined by its parent type.   
  
  
## I - Interface Segregation Principle (ISP)  

> **Should not be forced to implement methods it doesn’t need.**  

Instead of creating large, general-purpose interfaces, prefer smaller interfaces focused on specific needs.  
  
  
## D - Dependency Inversion Principle (DIP)  

> **Depend on abstractions, not concrete implementations.**  

High-level modules should not depend directly on low-level implementation details.  
Often achieved by using interfaces or other abstractions.  
  
  
