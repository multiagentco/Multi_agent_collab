 class Calculator:
    def add(self, num1: float, num2: float) -> float:
        """
        Adds two numbers.

        Args:
            num1 (float): The first number.
            num2 (float): The second number.

        Returns:
            float: The sum of num1 and num2.
        """
        return num1 + num2

    def subtract(self, num1: float, num2: float) -> float:
        """
        Subtracts num2 from num1.

        Args:
            num1 (float): The first number.
            num2 (float): The second number.

        Returns:
            float: The difference between num1 and num2.
        """
        return num1 - num2

    def multiply(self, num1: float, num2: float) -> float:
        """
        Multiplies two numbers.

        Args:
            num1 (float): The first number.
            num2 (float): The second number.

        Returns:
            float: The product of num1 and num2.
        """
        return num1 * num2

    def divide(self, num1: float, num2: float) -> float:
        """
        Divides num1 by num2.

        Args:
            num1 (float): The dividend.
            num2 (float): The divisor.

        Returns:
            float: The quotient of num1 and num2.

        Raises:
            ZeroDivisionError: If num2 is zero.
        """
        if num2 == 0:
            raise ZeroDivisionError("Cannot divide by zero")
        return num1 / num2

def main():
    calculator = Calculator()
    print(calculator.add(10, 5))  # Output: 15
    print(calculator.subtract(10, 5))  # Output: 5
    print(calculator.multiply(10, 5))  # Output: 50
    print(calculator.divide(10, 2))  # Output: 5.0

if __name__ == "__main__":
    main() 