 The Calculator class provides a simple implementation of a calculator with basic arithmetic operations. It includes methods for addition, subtraction, multiplication, and division.

### Calculator Class
```python
class Calculator:
    def add(self, a, b):
        """Returns the sum of two numbers."""
        return a + b

    def subtract(self, a, b):
        """Returns the difference between two numbers."""
        return a - b

    def multiply(self, a, b):
        """Returns the product of two numbers."""
        return a * b

    def divide(self, a, b):
        """
        Returns the quotient of two numbers.
        
        Raises:
            ZeroDivisionError: If the divisor is zero.
        """
        if b == 0:
            raise ZeroDivisionError("Cannot divide by zero")
        return a / b
```

### Example Usage
```python
calculator = Calculator()
print(calculator.add(5, 3))  # Output: 8
print(calculator.subtract(10, 4))  # Output: 6
print(calculator.multiply(7, 2))  # Output: 14
print(calculator.divide(9, 3))  # Output: 3.0
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
 if b ==0:
 raise ZeroDivisionError("Cannot divide by zero")
 return a / b
``` 