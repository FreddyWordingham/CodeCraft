# 🛠️ SOLID Principles

The SOLID principles are a set of principles that help us write better, more maintainable code.

They were coined by Robert C. Martin (Uncle Bob) in the year 2000 in his paper [Design Principles and Design Patterns](https://web.archive.org/web/20150906155800/http://www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf).

1. [👤 Single Responsibility Principle (SRP)](./solid/SRP.md)

   Each class should have one, and only one, reason to change.
   This principle advocates for having classes that are highly cohesive and focused on a single task or responsibility.

2. [🔒 Open/Closed Principle (OCP)](./solid/OCP.md)

   Software entities (like classes, modules, functions) should be open for extension, but closed for modification.
   This principle encourages us to write code that doesn’t have to be changed every time the requirements change.

3. [🔄 Liskov Substitution Principle (LSP)](./solid/LSP.md)

   Objects in a program should be replaceable with instances of their subtypes without altering the correctness of the program.
   This principle is key for achieving polymorphic behavior.

4. [🔌 Interface Segregation Principle (ISP)](./solid/ISP.md)

   No client should be forced to depend on methods it does not use.
   This principle suggests that it’s better to have many specific interfaces than one general-purpose interface.

5. [🔝 Dependency Inversion Principle (DIP)](./solid/DIP.md)

   High-level modules should not depend on low-level modules.
   Both should depend on abstractions.
   Abstractions should not depend on details.
   Details should depend on abstractions.
   This principle aims at reducing dependencies amongst the code modules.
