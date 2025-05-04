 The Python function `calculator(num1, num2, operation)` is defined to perform basic arithmetic operations. It takes three parameters: two numbers (`num1` and `num2`) and an `operation` to be performed. The function returns the result of the specified operation on the two numbers. The function handles addition, subtraction, multiplication, and division, and includes error handling for division by zero and invalid operations.

```python
def calculator(num1, num2, operation):
    """
    Performs basic arithmetic operations on two numbers.

    Args:
        num1 (float): The first number.
        num2 (float): The second number.
        operation (str): The operation to be performed. Can be 'add', 'subtract', 'multiply', or 'divide'.

    Returns:
        float: The result of the operation.
        str: Error message if division by zero or invalid operation.
    """
    if operation == 'add':
        return num1 + num2
    elif operation == 'subtract':
        return num1 - num2
    elif operation == 'multiply':
        return num1 * num2
    elif operation == 'divide':
        if num2 != 0:
            return num1 / num2
        else:
            return 'Error: Division by zero'
    else:
        return 'Error: Invalid operation'
```

Example use cases:
```python
print(calculator(10, 2, 'add'))  # Output: 12
print(calculator(10, 2, 'subtract'))  # Output: 8
print(calculator(10, 2, 'multiply'))  # Output: 20
print(calculator(10, 2, 'divide'))  # Output: 5.0
print(calculator(10, 0, 'divide'))  # Output: Error: Division by zero
print(calculator(10, 2, 'modulus'))  # Output: Error: Invalid operation
``` 