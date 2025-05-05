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