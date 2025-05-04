 ## Calculator Function Documentation
The Calculator class provides basic arithmetic operations such as addition, subtraction, multiplication, and division. The `calculator` function acts as an interface to these operations.

### Code
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

def calculator(a, b, operation):
    """
    Performs the specified arithmetic operation on two numbers.
    
    Args:
        a (float): The first operand.
        b (float): The second operand.
        operation (str): The operation to perform. Can be 'add', 'subtract', 'multiply', or 'divide'.
    
    Returns:
        float: The result of the operation.
    
    Raises:
        ValueError: If the operation is not one of the supported operations.
    """
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

if __name__ == "__main__":
    import unittest

    class TestCalculator(unittest.TestCase):
        def test_add(self):
            self.assertEqual(calculator(10, 5, 'add'), 15)
            self.assertEqual(calculator(-1, 1, 'add'), 0)
            self.assertEqual(calculator(-1, -1, 'add'), -2)

        def test_subtract(self):
            self.assertEqual(calculator(10, 5, 'subtract'), 5)
            self.assertEqual(calculator(-1, 1, 'subtract'), -2)
            self.assertEqual(calculator(-1, -1, 'subtract'), 0)

        def test_multiply(self):
            self.assertEqual(calculator(10, 5, 'multiply'), 50)
            self.assertEqual(calculator(-1, 1, 'multiply'), -1)
            self.assertEqual(calculator(-1, -1, 'multiply'), 1)

        def test_divide(self):
            self.assertEqual(calculator(10, 2, 'divide'), 5)
            self.assertEqual(calculator(-1, 1, 'divide'), -1)
            self.assertEqual(calculator(-1, -1, 'divide'), 1)
            self.assertRaises(ZeroDivisionError, calculator, 10, 0, 'divide')

        def test_invalid_operation(self):
            self.assertRaises(ValueError, calculator, 10, 5, 'modulus')

    unittest.main()
```

### Usage
To use the `calculator` function, simply call it with two numbers and the operation you want to perform. For example:
```python
result = calculator(10, 5, 'add')
print(result)  # Output: 15
``` 