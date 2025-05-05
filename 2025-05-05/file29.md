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

def main():
    print(calculator('add', 5, 3))
    print(calculator('subtract', 10, 4))
    print(calculator('multiply', 7, 2))
    print(calculator('divide', 9, 3))
    print(calculator('divide', 9, 0))
    print(calculator('modulus', 9, 3))

if __name__ == "__main__":
    main()
```