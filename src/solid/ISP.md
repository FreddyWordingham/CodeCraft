# 🔌 Interface Segregation Principle

The interface segregation principle (ISP) states that no client should be forced to depend on methods it does not use.

This principle is often misunderstood, and it is easy to fall into the trap of thinking that it is about interfaces.
The interface segregation principle is not about interfaces, but rather about the clients of a class or module.

## Bad Example: Not Following ISP

Suppose we modify the Shape interface to include a method for calculating the perimeter.
Not all shapes might need this method, but they are forced to implement it.

```python
class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass

class Rectangle(Shape):
    # Area implementation
    def perimeter(self):
        return 2 * (self.length + self.width)

class Circle(Shape):
    # Area implementation
    def perimeter(self):
        return 2 * 3.14 * self.radius

class Triangle(Shape):
    # Area implementation
    # Triangle might not need a perimeter method, but it's forced to implement it
    def perimeter(self):
        pass  # Not applicable or not needed for some triangles
```

This is bad because the Triangle class is forced to implement a method that it doesn't need.

## Good Example: Following ISP

Refactor by creating separate interfaces for area and perimeter calculations, so that each shape only implements the necessary interfaces.

```python
class Area(ABC):
    @abstractmethod
    def area(self):
        pass

class Perimeter(ABC):
    @abstractmethod
    def perimeter(self):
        pass

class Rectangle(Area, Perimeter):
    # Implement both area and perimeter

class Circle(Area, Perimeter):
    # Implement both area and perimeter

class Triangle(Area):
    # Implement only area, no need for perimeter
```

This design adheres to ISP, as each shape class only implements the interfaces it needs.
Triangle is not forced to depend on the perimeter method, which it might not use.

## Recap

- The **bad example** demonstrates how enforcing a common interface with methods that are not universally applicable can lead to awkward and potentially problematic implementations.
  The Triangle class having to implement a perimeter method that it doesn't need is a clear violation of ISP.
  This leads to bloated interfaces and can cause confusion and errors, especially if dummy implementations are used.
- The **good example** is a great demonstration of adhering to ISP.
  By separating the concerns into two interfaces, Area and Perimeter, each class implements only what is necessary for its purpose.
  This approach makes the system more flexible and easier to understand.
  It also enhances maintainability, as changes in the calculation of the area or perimeter only affect relevant classes.

Key points about ISP:

- **Client-Centric Design**: ISP emphasizes designing from the client's perspective.
  Classes shouldn't be burdened with irrelevant methods just because they share some common features with other classes.
- **Reduced Impact of Changes**: By segregating interfaces, changes in one part of the system are less likely to affect unrelated parts.
- **Ease of Understanding and Maintenance**: Smaller, well-defined interfaces are easier to understand and implement correctly.

Implementing ISP correctly is crucial for creating clean, maintainable code.
It ensures that classes only have the dependencies they need, which is especially important in large systems where unnecessary dependencies can significantly complicate the codebase.
