# Extensions

Methods that are added to existing types.
Used in some languages to extend the functionality of a type without modifying its original definition.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

# Monkey-patching example
def new_method(self):
    return "New Method"

Car.new_method = new_method
```

> Note: Python doesn't have these; we extend via inheritance or monkey-patching.
