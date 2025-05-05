 ## Calculator Class Documentation
### Overview

The `Calculator` class provides basic arithmetic operations such as addition, subtraction, multiplication, and division.

### Methods

#### `add(num1: float, num2: float) -> float`

* Adds two numbers.
* Args:
 * `num1 (float)`: The first number.
 * `num2 (float)`: The second number.
* Returns:
 * `float`: The sum of `num1` and `num2`.

#### `subtract(num1: float, num2: float) -> float`

* Subtracts `num2` from `num1`.
* Args:
 * `num1 (float)`: The first number.
 * `num2 (float)`: The second number.
* Returns:
 * `float`: The difference between `num1` and `num2`.

#### `multiply(num1: float, num2: float) -> float`

* Multiplies two numbers.
* Args:
 * `num1 (float)`: The first number.
 * `num2 (float)`: The second number.
* Returns:
 * `float`: The product of `num1` and `num2`.

#### `divide(num1: float, num2: float) -> float`

* Divides `num1` by `num2`.
* Args:
 * `num1 (float)`: The dividend.
 * `num2 (float)`: The divisor.
* Returns:
 * `float`: The quotient of `num1` and `num2`.
* Raises:
 * `ZeroDivisionError`: If `num2` is zero.

### Example Usage

```python
calculator = Calculator()
print(calculator.add(10,5)) # Output:15
print(calculator.subtract(10,5)) # Output:5
print(calculator.multiply(10,5)) # Output:50
print(calculator.divide(10,2)) # Output:5.0
```

### Commit Message

`Added Calculator class with basic arithmetic operations`

### API Documentation

You can generate API documentation using tools like Sphinx or Pydoc. For example, you can use the following command to generate HTML documentation using Pydoc:

```bash
pydoc -w calculator
```

This will generate an HTML file `calculator.html` in the current directory. 