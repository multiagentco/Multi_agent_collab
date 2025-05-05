

Development: Create a Python class that represents a calculator with methods for basic arithmetic operations like addition, subtraction, multiplication, and division.
Testing: Write unit tests using Python's unittest framework to validate the calculator's functionality by checking the results of various operations.
Documentation: Generate documentation for the calculator class using Python docstrings, explaining the purpose, parameters, and return values of each method.



```python
def calculator(operation, a, b):
    if operation == 'add':
        return a + b
    elif operation == 'subtract':
        return a - b
    elif operation == 'multiply':
        return a * b
    elif operation == 'divide':
        if b == 0:
            raise ZeroDivisionError('Cannot divide by zero')
        return a / b
    else:
        raise ValueError('Invalid operation')
```



```python
assert calculator('add', 5, 3) == 8
assert calculator('divide', 10, 2) == 5
assert calculator('multiply', 4, 5) == 20
```



## Calculator Function Documentation
The `calculator` function performs basic arithmetic operations on two numbers.

### Parameters
* `operation` (str): The operation to be performed. Can be 'add', 'subtract', 'multiply', or 'divide'.
* `a` (int or float): The first operand.
* `b` (int or float): The second operand.

### Returns
* The result of the operation.

### Raises
* `ZeroDivisionError`: If `operation` is 'divide' and `b` is 0.
* `ValueError`: If `operation` is not one of the supported operations.

### Example Usage
```python
print(calculator('add', 5, 3))  # Output: 8
print(calculator('subtract', 10, 4))  # Output: 6
print(calculator('multiply', 4, 5))  # Output: 20
print(calculator('divide', 10, 2))  # Output: 5.0
```

```python
def calculator(operation, a, b):
 if operation == 'add':
 return a + b
 elif operation == 'subtract':
 return a - b
 elif operation == 'multiply':
 return a * b
 elif operation == 'divide':
 if b ==0:
 raise ZeroDivisionError('Cannot divide by zero')
 return a / b
 else:
 raise ValueError('Invalid operation')
```

