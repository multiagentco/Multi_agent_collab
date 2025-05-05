## Calculator Function
The `calculator` function performs basic arithmetic operations on two numbers.

### Parameters
* `operation` (str): The operation to be performed. Can be 'add', 'subtract', 'multiply', or 'divide'.
* `a` (int or float): The first operand.
* `b` (int or float): The second operand.

### Returns
* The result of the operation.

### Raises
* `ZeroDivisionError`: If `operation` is 'divide' and `b` is zero.
* `ValueError`: If `operation` is not one of the supported operations.

### Example
```python
result = calculator('add', 5, 3)
print(result)  # Output: 8
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