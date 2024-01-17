# 🔒 Open/Closed Principle

The open/closed principle (OCP) states that software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification.

Simply put, this means that we should write code that doesn't have to be changed every time the requirements change.

This principle is often misunderstood, and it is easy to fall into the trap of thinking that we should never change code once it has been written.
The open/closed principle is not about never changing code, but rather about writing code that is easy to change.

## Bad Example: Not Following Open/Closed Principle

Imagine a simple Shape class that calculates the area of different shapes.
Initially, it only handles rectangles.

```python
class Shape:
    def __init__(self, shape_type, dimensions):
        self.shape_type = shape_type
        self.dimensions = dimensions

    def area(self):
        if self.shape_type == "rectangle":
            return self.dimensions['length'] * self.dimensions['width']
        # Adding a new shape means modifying this method

# Usage
rectangle = Shape("rectangle", {"length": 5, "width": 10})
print("Area:", rectangle.area())
```

Problem: To add a new shape (e.g., circle), we must modify the Shape class, violating the open/closed principle.

## Good Example: Following Open/Closed Principle

Let's refactor using polymorphism.
Create an abstract Shape class and extend it for each specific shape.

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

# Usage
shapes = [Rectangle(5, 10), Circle(7)]
for shape in shapes:
    print("Area:", shape.area())
```

This design is open for extension (easy to add new shapes) but closed for modification (no need to change existing code).

## Recap

- In the **bad example**, the need to modify the Shape class for each new shape type shows how the design is not sustainable.
  This approach leads to a class that's difficult to maintain and prone to errors, especially as the system grows and evolves.
- The **good example** illustrates the right approach by using polymorphism.
  By defining an abstract Shape class and extending it for specific shapes, we adhere to OCP.
  This design allows new shape types to be added (like Circle, Triangle, etc.) without altering the existing code.
  Each shape class encapsulates its own logic for calculating the area, adhering to both OCP and SRP.

This approach has several advantages:

- **Maintainability**: It's easier to understand and maintain separate classes, each responsible for the behavior of a specific shape.
- **Scalability**: Adding a new shape is as simple as creating a new class that extends Shape.
- **Reduced Risk of Bugs**: Changes to one shape type don't affect others, reducing the risk of introducing bugs.
- **Testing**: Each shape can be tested independently, leading to more robust and reliable code.

The essence of OCP is to write code that accommodates future growth and change with minimal modification to existing code.
It's a key principle in building scalable and flexible systems.
