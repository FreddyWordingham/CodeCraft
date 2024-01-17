# 🔝 Dependency Inversion Principle

The dependency inversion principle (DIP) states that high-level modules should not depend on low-level modules.
Both should depend on abstractions.
Abstractions should not depend on details.
Details should depend on abstractions.

This principle is often misunderstood, and it is easy to fall into the trap of thinking that it is about dependency injection.
The dependency inversion principle is not about dependency injection, but rather about the direction of dependencies.

## Bad Example: Not Following DIP

Suppose we have a high-level module that depends on a low-level module.

```python
class EmployeeManager:
    def __init__(self, employee_database):
        self.employee_database = employee_database

    def add_employee(self, employee):
        self.employee_database.add(employee)

    def remove_employee(self, employee_id):
        self.employee_database.remove(employee_id)
```

This is bad because the high-level module (EmployeeManager) depends on the low-level module (employee_database).
If the low-level module changes, the high-level module must change too.

## Good Example: Following DIP

Refactor by introducing an abstraction (interface) between the high-level and low-level modules.

```python
class EmployeeDatabase(ABC):
    @abstractmethod
    def add(self, employee):
        pass

    @abstractmethod
    def remove(self, employee_id):
        pass
```

This design adheres to DIP, as the high-level module (EmployeeManager) depends on an abstraction (EmployeeDatabase) instead of a low-level module.
If the low-level module changes, the high-level module doesn't need to change.

## Recap

- In the **bad example**, the direct dependency of EmployeeManager on a concrete employee_database implementation exemplifies a violation of DIP.
  This tight coupling makes the high-level module (EmployeeManager) susceptible to changes in the low-level module (employee_database), which is undesirable.
  Such a design makes the system rigid and hard to maintain, especially when changes or new requirements emerge.
- The **good example** demonstrates the proper implementation of DIP.
  By introducing an abstract EmployeeDatabase interface, EmployeeManager becomes dependent on an abstraction rather than a concrete implementation.
  This decouples the high-level module from the details of the low-level module, allowing for greater flexibility.
  If the implementation of the database changes, EmployeeManager remains unaffected, as it relies solely on the interface.

Key aspects of DIP:
- **Decoupling**: It promotes loose coupling between classes, which enhances modularity and makes the system more resilient to changes.
- **Flexibility**: It allows for easier substitution of modules.
  For example, switching from one database implementation to another becomes trivial.
- **Maintainability**: Changes in low-level modules don’t necessitate changes in high-level modules, reducing the maintenance burden.

It's important to note that while DIP and Dependency Injection (DI) are related, they are not the same.
DI is a technique for achieving DIP, typically involving frameworks that automatically handle the creation and binding of dependencies.
DIP, on the other hand, is a broader design principle aimed at reducing dependencies between high-level and low-level modules.

Our application of DIP enhances the design and maintainability of our code, aligning with best practices in software architecture.
