# Traits

Shared behaviour definitions that can be mixed into classes.
Useful for sharing functionality across different classes, promoting code reuse.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

class ElectricVehicleMixin:
    def charge(self):
        return "Charging..."

class ElectricCar(Car, ElectricVehicleMixin):
    pass

my_car = ElectricCar("Tesla", "Model S")
```

> Python uses mixins for similar functionality.
