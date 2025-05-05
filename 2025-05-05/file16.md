 ## Calculator Documentation
The Calculator class provides basic arithmetic operations such as addition, subtraction, multiplication, and division. It is designed to be used through the `calculator` function, which instantiates the Calculator class and performs the specified operation.

### Calculator Class
#### Methods
- `add(a, b)`: Returns the sum of `a` and `b`.
- `subtract(a, b)`: Returns the difference of `a` and `b`.
- `multiply(a, b)`: Returns the product of `a` and `b`.
- `divide(a, b)`: Returns the quotient of `a` and `b`. Raises a `ZeroDivisionError` if `b` is zero.

### calculator Function
#### Parameters
- `a`: The first operand.
- `b`: The second operand.
- `operation`: A string specifying the operation to perform. Can be 'add', 'subtract', 'multiply', or 'divide'.

#### Returns
The result of the specified operation on `a` and `b`.

#### Raises
- `ValueError`: If `operation` is not one of the supported operations.
- `ZeroDivisionError`: If `operation` is 'divide' and `b` is zero.

### Example Usage
```python
print(calculator(10, 2, 'add'))  # Output: 12
print(calculator(10, 2, 'subtract'))  # Output: 8
print(calculator(10, 2, 'multiply'))  # Output: 20
print(calculator(10, 2, 'divide'))  # Output: 5.0
```

### Code
```python
class Calculator:
    def add(self, a, b):
        return a + b

    def subtract(self, a, b):
        return a - b

    def multiply(self, a, b):
        return a * b

    def divide(self, a, b):
        if b == 0:
            raise ZeroDivisionError("Cannot divide by zero")
        return a / b

def calculator(a, b, operation):
    calc = Calculator()
    if operation == 'add':
        return calc.add(a, b)
    elif operation == 'subtract':
        return calc.subtract(a, b)
    elif operation == 'multiply':
        return calc.multiply(a, b)
    elif operation == 'divide':
        return calc.divide(a, b)
    else:
        raise ValueError("Invalid operation")
``` 