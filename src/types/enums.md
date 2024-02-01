# Enums

Enumerations, a way to define a type by enumerating its possible values. Useful for representing a fixed set of related constants, like days of the week, states in a state machine, etc.

```python
from enum import Enum

class Color(Enum):
    RED = 1
    GREEN = 2
    BLUE = 3

color = Color.RED
```
