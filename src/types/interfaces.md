# Interfaces

Definitions of methods that a class must implement.
Used for defining a common contract for different classes, promoting consistency and interoperability.

```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start_engine(self):
        """Start the engine of the vehicle"""
        pass

class Car(Vehicle):
    def start_engine(self):
        return "Car engine started"

# Usage
my_car = Car()
print(my_car.start_engine())  # Outputs: Car engine started
```
