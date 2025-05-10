

Development: Create a Python class named 'Calculator' that includes methods for basic arithmetic operations like addition, subtraction, multiplication, and division.
Testing: Write unit tests using Python's unittest framework to validate the Calculator class methods for different input scenarios.
Documentation: Generate documentation for the Calculator class and its methods using Python docstrings, explaining the purpose, parameters, and return values.



```python
def calculator(operation, a, b):
    if operation == 'add':
        return a + b
    elif operation == 'subtract':
        return a - b
    elif operation == 'multiply':
        return a * b
    elif operation == 'divide':
        if b != 0:
            return a / b
        else:
            return 'Error: Division by zero'
    else:
        return 'Error: Invalid operation'
```



```python
assert calculator('add', 5, 3) == 8
assert calculator('divide', 10, 2) == 5.0
assert calculator('divide', 10, 0) == 'Error: Division by zero'
```



## Calculator Function Documentation
The `calculator` function performs basic arithmetic operations on two numbers.

### Function Signature
```python
def calculator(operation, a, b):
```

### Parameters

* `operation` (str): The arithmetic operation to perform. Can be one of 'add', 'subtract', 'multiply', or 'divide'.
* `a` (int or float): The first operand.
* `b` (int or float): The second operand.

### Return Value

* The result of the arithmetic operation. If the operation is 'divide' and `b` is zero, returns 'Error: Division by zero'. If the operation is not one of the four basic arithmetic operations, returns 'Error: Invalid operation'.

### Example Usage
```python
print(calculator('add', 5, 3))  # Output: 8
print(calculator('subtract', 10, 4))  # Output: 6
print(calculator('multiply', 7, 2))  # Output: 14
print(calculator('divide', 10, 2))  # Output: 5.0
print(calculator('divide', 10, 0))  # Output: Error: Division by zero
print(calculator('modulus', 10, 3))  # Output: Error: Invalid operation
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
 if b !=0:
 return a / b
 else:
 return 'Error: Division by zero'
 else:
 return 'Error: Invalid operation'
```

