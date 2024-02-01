# Unions

A type that can be one of several types.
Common in type systems that support type-checking for multiple types, useful for functions that can accept different types and for modelling data that can be in different forms.

```python
from typing import Union

Number = Union[int, float]

def add_numbers(a: Number, b: Number) -> Number:
    return a + b
```
