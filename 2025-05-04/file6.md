 The Calculator class provides methods for performing basic arithmetic operations. It includes methods for addition, subtraction, multiplication, and division, each taking two numbers as input and returning the result of the operation. The calculator function acts as an interface to these methods, allowing users to specify the operation to be performed. The code is well-structured and follows standard professional guidelines for documentation and error handling.

```python
class Calculator:
 def add(self, a, b):
 """Adds two numbers.
        
 Args:
 a (float): The first number.
 b (float): The second number.
        
 Returns:
 float: The sum of a and b.
 """
 return a + b
    
 def subtract(self, a, b):
 """Subtracts b from a.
        
 Args:
 a (float): The first number.
 b (float): The second number.
        
 Returns:
 float: The difference between a and b.
 """
 return a - b
    
 def multiply(self, a, b):
 """Multiplies two numbers.
        
 Args:
 a (float): The first number.
 b (float): The second number.
        
 Returns:
 float: The product of a and b.
 """
 return a * b
    
 def divide(self, a, b):
 """Divides a by b.
        
 Args:
 a (float): The dividend.
 b (float): The divisor.
        
 Returns:
 float: The quotient of a and b.
        
 Raises:
 ZeroDivisionError: If b is zero.
 """
 if b ==0:
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

# Example usage
print(calculator(10,2, 'add')) # Output:12
print(calculator(10,2, 'subtract')) # Output:8
print(calculator(10,2, 'multiply')) # Output:20
print(calculator(10,2, 'divide')) # Output:5.0
``` 