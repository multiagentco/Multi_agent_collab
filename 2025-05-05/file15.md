 The Calculator class provides methods for performing basic arithmetic operations. It includes methods for addition, subtraction, multiplication, and division. The division method raises a ZeroDivisionError if the divisor is zero. 

```python
class Calculator:
 def add(self, a, b):
 """Return the sum of two numbers."""
 return a + b

 def subtract(self, a, b):
 """Return the difference between two numbers."""
 return a - b

 def multiply(self, a, b):
 """Return the product of two numbers."""
 return a * b

 def divide(self, a, b):
 """Return the quotient of two numbers. Raises ZeroDivisionError if divisor is zero."""
 if b == 0:
 raise ZeroDivisionError("Cannot divide by zero")
 return a / b
``` 