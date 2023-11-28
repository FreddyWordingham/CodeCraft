# Introduction

## 🏆 Why should we care about good code?

-   **Satisfaction**: Meets user needs, ensuring loyalty.
-   **Maintainability**: Easier updates, saves time and resources.
-   **Reliability**: Reduces downtime and errors.
-   **Scalability**: Easily adapts to growing demands.
-   **Security**: Robust features protect against breaches.
-   **Reputation**: Enhances team credibility, opens opportunities.

### Example

Here is a simple Python function to calculate the factorial of a number.

```python
def factorial(n):
    if (n == 0 or n == "0"):
        return 1
    elif (str(n).isdigit() and int(n) > 0):
        fact = 1
        i = 1
        while (i <= n):
            fact = fact * i
            i += 1
        return fact
    else:
        return "Error"
```

This function is not good code.
It is difficult to read, difficult to understand, and difficult to maintain.
It is also not very efficient, and does not handle errors well.

-   Poor input validation: mixes string and integer types.
-   Inefficient and unclear looping structure.
-   Returns mixed data types (integers and strings), which is a bad practice.
-   No comments or documentation.

Overall it leaves us with a distinct feeling of unease, sadness, and despair.

Let's have a look at a comparatively good implementation of the same function.

```python
@typechecked
def factorial(n: int):
    if n < 0:
        raise ValueError("Input must be a non-negative integer")
    if n == 0:
        return 1
    return n * factorial(n-1)
```

Improvements:

-   Clear and strict input validation with meaningful error messages.
-   Uses recursion, which is a more elegant and Pythonic approach for this problem.
-   Consistent return type, raising exceptions for invalid inputs.

This is a much better implementation.
Notice the warm feeling of satisfaction and joy that it gives us.
