 I can help you generate documentation for the calculator function.

## Calculator Function Documentation
### Overview
The `calculator` function performs basic arithmetic operations on two numbers.

### Parameters
* `operation` (str): The operation to be performed. Can be 'add', 'subtract', 'multiply', or 'divide'.
* `a` (int or float): The first operand.
* `b` (int or float): The second operand.

### Returns
* The result of the operation if successful.
* 'Error: Division by zero' if division by zero is attempted.
* 'Error: Invalid operation' if an invalid operation is specified.

### Example Usage
```python
print(calculator('add', 5, 3))  # Output: 8
print(calculator('subtract', 10, 4))  # Output: 6
print(calculator('multiply', 7, 2))  # Output: 14
print(calculator('divide', 9, 3))  # Output: 3.0
``` 