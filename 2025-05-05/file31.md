def calculator(operation, a, b):
    """
    Performs basic arithmetic operations.

    Args:
        operation (str): The operation to perform. Can be 'add', 'subtract', 'multiply', or 'divide'.
        a (float): The first operand.
        b (float): The second operand.

    Returns:
        float: The result of the operation.
        str: An error message if the operation is invalid or if division by zero occurs.
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

def main():
    """
    Tests the calculator function with various operations.
    """
    print(calculator('add', 5, 3))
    print(calculator('subtract', 10, 4))
    print(calculator('multiply', 7, 2))
    print(calculator('divide', 9, 3))
    print(calculator('divide', 9, 0))
    print(calculator('modulus', 9, 3))

if __name__ == "__main__":
    main()