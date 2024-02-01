# Delegates

References to methods, treating them as first-class objects.
Used for callback functions, event handling, and defining function parameters that can be passed around and invoked.

```python
def my_function():
    return "Hello"

delegate = my_function

print(delegate())
```
