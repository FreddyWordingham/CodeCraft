# Objects

Instances of classes.
Represent individual entities with their own state and behaviour defined by their class.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model


# These are the objects:
my_car = Car("Toyota", "Corolla")
another_car = Car("Ford", "Fiesta")
```
