 The Python function `calculator(a, b, operation)` performs basic arithmetic operations on two numbers, `a` and `b`, based on the specified `operation`. The supported operations are 'add', 'subtract', 'multiply', and 'divide'. It returns the result of the operation or an error message if the operation is invalid or if division by zero is attempted. The function is designed to be used with valid numeric inputs for `a` and `b`, and a string indicating the operation to be performed. Example usage is provided to demonstrate how to use the function with different operations. 

```python
def calculator(a, b, operation):
    """
    Performs basic arithmetic operations on two numbers.

    Args:
        a (float): The first number.
        b (float): The second number.
        operation (str): The operation to be performed. Supported operations are 'add', 'subtract', 'multiply', and 'divide'.

    Returns:
        float: The result of the operation.
        str: An error message if the operation is invalid or if division by zero is attempted.
    """
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

# Example usage:
print(calculator(10, 2, 'add'))  # Output: 12
print(calculator(10, 2, 'subtract'))  # Output: 8
print(calculator(10, 2, 'multiply'))  # Output: 20
print(calculator(10, 2, 'divide'))  # Output: 5.0
print(calculator(10, 0, 'divide'))  # Output: Error: Division by zero
print(calculator(10, 2, 'modulus'))  # Output: Error: Invalid operation
``` 