 class Calculator:
    def add(self, a, b):
        """Return the sum of two numbers."""
        return a + b

    def subtract(self, a, b):
        """Return the difference of two numbers."""
        return a - b

    def multiply(self, a, b):
        """Return the product of two numbers."""
        return a * b

    def divide(self, a, b):
        """
        Return the quotient of two numbers.

        Args:
            a (float): The dividend.
            b (float): The divisor.

        Returns:
            float: The quotient of a and b.

        Raises:
            ZeroDivisionError: If b is zero.
        """
        if b == 0:
            raise ZeroDivisionError("Cannot divide by zero")
        return a / b

def calculator(a, b, operation):
    """
    Perform a basic arithmetic operation on two numbers.

    Args:
        a (float): The first operand.
        b (float): The second operand.
        operation (str): The operation to perform. Can be 'add', 'subtract', 'multiply', or 'divide'.

    Returns:
        float: The result of the operation.

    Raises:
        ValueError: If the operation is not one of the four basic arithmetic operations.
    """
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