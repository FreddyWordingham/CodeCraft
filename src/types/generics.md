# Generics

Parameterized types, allowing the creation of components that work with any type.
Useful for creating reusable and type-safe data structures and algorithms.

```python
from typing import Generic, TypeVar

T = TypeVar('T')

class Box(Generic[T]):
    def __init__(self, item: T):
        self.item = item

int_box = Box[int](123)
```
