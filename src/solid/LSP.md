# 🔄 Liskov Substitution Principle

The Liskov substitution principle states that objects in a program should be replaceable with instances of their subtypes without altering the correctness of the program.

This principle is often misunderstood, and it is easy to fall into the trap of thinking that it is about inheritance.
The Liskov substitution principle is not about inheritance, but rather about the behavior of subtypes.

> Liskov is named after Barbara Liskov, who first wrote about it in a 1987 conference keynote address titled Data abstraction and hierarchy.
> She based it on the earlier work of Jeannette Wing, who wrote about it in a 1980 paper titled A notion of correctness for object-oriented programs.
> Barbara Liskov and Jeannette Wing are two of the most influential computer scientists of all time, and they are both still alive today.
> They are both professors at MIT, and they are both still actively involved in research.
> In 1968 Barbara became one of the first women in the United States to be awarded a computer science PhD.
> Her thesis on chess end-games was supervised by John McCarthy.
> Barbara Liskov won the Turing Award in 2008, and Jeannette Wing won the Dijkstra Prize in 2011.

## Bad Example: Not Following LSP

Let's continue with the Shape example from the previous section.
Imagine that we want to add a Square class that extends the Rectangle class.

```python
class Square(Rectangle):
    def __init__(self, side):
        super().__init__(side, side)

    def set_width(self, width):
        self.width = self.length = width

    def set_length(self, length):
        self.length = self.width = length

# Usage
def process_shape(r: Rectangle):
    r.set_width(10)
    return r.area()

square = Square(5)
print("Expected area of 5x10 square:", process_shape(square))  # Incorrectly returns 100
```

This is bad because changing the width of a Square changes its length too, which is unexpected for a Rectangle.
It breaks the LSP as Square cannot be substituted for Rectangle without altering the program's behavior.

## Good Example: Following LSP

Instead of inheritance, use a common interface or separate classes for shapes that don't share properties.

```python
class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Rectangle(Shape):
    # Same as before

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side * self.side

# Usage remains the same
```

In this design, Square and Rectangle are separate entities
There's no unexpected behavior when a Square is used in place of a Rectangle because they are not interchangeable, adhering to LSP.

## Recap

- In the **bad example**, Square extending Rectangle leads to a violation of LSP.
  It's tempting to use inheritance here because a square is a special kind of rectangle, but this relationship doesn't hold up in code when their behaviors (like setting width or length) differ.
  When a Square object replaces a Rectangle object, it breaks the expectations of how a Rectangle should behave, specifically in the process_shape function.
- The **good example** correctly addresses this by treating Square and Rectangle as separate entities that both implement a common Shape interface.
    This approach respects LSP, as each class can be substituted for a Shape without changing the correctness of the program.
    Here, there's no assumption or requirement that a Square must behave like a Rectangle.

A few key takeaways about LSP:
- **Behavioral Subtyping**: LSP is essentially about behavioral subtyping.
  Subtypes should be able to replace their base types without altering the desired behavior of the program.
- **Design Thoughtfulness**: It encourages careful thought when using inheritance.
  Not all "is-a" relationships in the real world translate well to code.
- **Robustness**: Adhering to LSP leads to more robust and flexible code, where components can be easily interchanged without causing issues.

Implementing LSP properly often leads to better abstraction in our code, allowing for more flexible and reusable components.
