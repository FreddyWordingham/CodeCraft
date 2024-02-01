# Records

Immutable data structures, often with named fields.
Used for representing simple data objects where modification after creation is not required.

```python
from dataclasses import dataclass

@dataclass(frozen=True)
class Point:
    x: int
    y: int

point = Point(1, 2)
```

> Note: Python doesn't have records, but dataclasses can be used similarly.
