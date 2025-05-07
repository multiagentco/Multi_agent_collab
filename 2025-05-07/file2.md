

Development: Create a Python class named 'Calculator' that includes methods for basic arithmetic operations like addition, subtraction, multiplication, and division.
Testing: Write unit tests using Python's unittest framework to validate the Calculator class methods for different input scenarios.
Documentation: Generate documentation for the Calculator class and its methods using Python docstrings, explaining the purpose, parameters, and return values.



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
```



```python
assert calculator('add', 5, 3) == 8
assert calculator('divide', 10, 2) == 5.0
assert calculator('divide', 10, 0) == 'Error: Division by zero'
```



## Calculator Function Documentation
The `calculator` function performs basic arithmetic operations on two numbers.

### Function Signature
```python
def calculator(operation, a, b):
```

### Parameters

* `operation` (str): The arithmetic operation to be performed. Supported operations are 'add', 'subtract', 'multiply', and 'divide'.
* `a` (int or float): The first operand.
* `b` (int or float): The second operand.

### Return Value

* The result of the arithmetic operation. If the operation is 'divide' and `b` is zero, returns 'Error: Division by zero'. If the operation is not supported, returns 'Error: Invalid operation'.

### Example Usage
```python
print(calculator('add', 5, 3))  # Output: 8
print(calculator('subtract', 10, 4))  # Output: 6
print(calculator('multiply', 7, 2))  # Output: 14
print(calculator('divide', 10, 2))  # Output: 5.0
print(calculator('divide', 10, 0))  # Output: Error: Division by zero
print(calculator('invalid_op', 5, 3))  # Output: Error: Invalid operation
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
 if b !=0:
 return a / b
 else:
 return 'Error: Division by zero'
 else:
 return 'Error: Invalid operation'
```



Development: Create a Python class or function that implements a simple number guessing game, where the user has to guess a randomly generated number within a specified range.
Testing: Write unit tests using Python's unittest framework to validate the game's functionality, such as checking if the game correctly identifies a winning guess.
Documentation: Generate documentation for the game using Python docstrings, explaining the rules, parameters, and return values.



```python
import random

def number_game(min_val, max_val):
 number_to_guess = random.randint(min_val, max_val)
 attempts = 0

 while True:
 try:
 user_guess = int(input(f"Guess a number between {min_val} and {max_val}: "))
 attempts += 1

 if user_guess < number_to_guess:
 print("Too low!")
 elif user_guess > number_to_guess:
 print("Too high!")
 else:
 print(f"Congratulations! You've guessed the number in {attempts} attempts.")
 break
 except ValueError:
 print("Invalid input. Please enter a valid number.")

# Example usage
number_game(1, 100)
```



import unittest
from unittest.mock import patch
from io import StringIO

class TestNumberGame(unittest.TestCase):

 @patch('sys.stdout', new_callable=StringIO)
 @patch('builtins.input', side_effect=['50', '75', '67', '68'])
 def test_number_game_winning_guess(self, mock_input, mock_stdout):
 number_game(1, 100)
 self.assertIn("Congratulations!", mock_stdout.getvalue())

 @patch('sys.stdout', new_callable=StringIO)
 @patch('builtins.input', side_effect=['abc', '50'])
 def test_number_game_invalid_input(self, mock_input, mock_stdout):
 number_game(1, 100)
 self.assertIn("Invalid input.", mock_stdout.getvalue())

if __name__ == '__main__':
 unittest.main()



## Number Game Function Documentation
The `number_game` function implements a simple number guessing game.

### Function Signature
```python
def number_game(min_val, max_val):
```

### Parameters

* `min_val` (int): The minimum value of the range (inclusive).
* `max_val` (int): The maximum value of the range (inclusive).

### Functionality

1. Generates a random number between `min_val` and `max_val` (inclusive).
2. Continuously prompts the user to guess the number until the correct guess is made.
3. Provides feedback on the user's guess, indicating if it's too low or too high.
4. Displays a congratulatory message with the number of attempts taken to guess the number correctly.

### Example Usage
```python
number_game(1,100)
```

### Notes

* The function uses `random.randint` to generate a random number within the specified range.
* The game continues until the user guesses the number correctly.
* Invalid inputs (non-integer values) are handled and prompt the user to re-enter a valid number.

