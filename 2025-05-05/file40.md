Development: Create a Python class that represents a calculator with methods for basic arithmetic operations like addition, subtraction, multiplication, and division.
Testing: Write unit tests using Python's unittest framework to validate the calculator's functionality by checking the results of various arithmetic operations.
Documentation: Generate documentation for the calculator class using Python docstrings, explaining the purpose, parameters, and return values of each method.```python
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
``````python
assert calculator('add', 5, 3) == 8
assert calculator('divide', 9, 0) == 'Error: Division by zero'
assert calculator('modulus', 9, 3) == 'Error: Invalid operation'
```## Calculator Function Documentation
The `calculator` function performs basic arithmetic operations on two numbers.

### Parameters
* `operation` (str): The arithmetic operation to be performed. Supported operations are 'add', 'subtract', 'multiply', and 'divide'.
* `a` (int or float): The first operand.
* `b` (int or float): The second operand.

### Returns
* The result of the arithmetic operation if successful.
* 'Error: Division by zero' if division by zero is attempted.
* 'Error: Invalid operation' if an unsupported operation is specified.

### Example Usage
```python
print(calculator('add', 5, 3))  # Output: 8
print(calculator('subtract', 10, 4))  # Output: 6
print(calculator('multiply', 7, 2))  # Output: 14
print(calculator('divide', 9, 3))  # Output: 3.0
print(calculator('divide', 9, 0))  # Output: 'Error: Division by zero'
print(calculator('modulus', 9, 3))  # Output: 'Error: Invalid operation'
```

```python
def calculator(operation, a, b):
 """
 Performs basic arithmetic operations on two numbers.

 Args:
 operation (str): The arithmetic operation to be performed.
 a (int or float): The first operand.
 b (int or float): The second operand.

 Returns:
 The result of the arithmetic operation if successful.
 'Error: Division by zero' if division by zero is attempted.
 'Error: Invalid operation' if an unsupported operation is specified.
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
 print(calculator('add', 5, 3))
 print(calculator('subtract', 10, 4))
 print(calculator('multiply', 7, 2))
 print(calculator('divide', 9, 3))
 print(calculator('divide', 9, 0))
 print(calculator('modulus', 9, 3))

if __name__ == "__main__":
 main()
```Development: Create a Python program that implements a number guessing game where the user has to guess a randomly generated number within a specified range.
Testing: Write unit tests using Python's unittest framework to validate the game's functionality, including checking the game's response to correct and incorrect guesses.
Documentation: Generate documentation for the number game using Python docstrings, explaining the game's rules, parameters, and return values.```python
import random

def number_game(min_value, max_value):
 number_to_guess = random.randint(min_value, max_value)
 attempts = 0
 while True:
 user_guess = input(f'Guess a number between {min_value} and {max_value}: ')
 try:
 user_guess = int(user_guess)
 attempts += 1
 if user_guess < number_to_guess:
 print('Too low!')
 elif user_guess > number_to_guess:
 print('Too high!')
 else:
 print(f'Congratulations! You found the number in {attempts} attempts.')
 break
 except ValueError:
 print('Invalid input. Please enter a number.')

def main():
 number_game(1,100)

if __name__ == "__main__":
 main()
``````python
import unittest
from unittest.mock import patch
from your_module import number_game  # Replace 'your_module' with the actual name of your module

class TestNumberGame(unittest.TestCase):

 @patch('builtins.input', side_effect=['50', '75', '67'])
 @patch('builtins.print')
 def test_number_game(self, mock_print, mock_input):
 with patch('random.randint', return_value=67):
 number_game(1, 100)
 mock_print.assert_called_with('Congratulations! You found the number in 3 attempts.')

 @patch('builtins.input', side_effect=['a', '50'])
 @patch('builtins.print')
 def test_invalid_input(self, mock_print, mock_input):
 with patch('random.randint', return_value=50):
 number_game(1, 100)
 mock_print.assert_any_call('Invalid input. Please enter a number.')

if __name__ == '__main__':
 unittest.main(argv=[''], exit=False)
```## Number Game Function Documentation
The `number_game` function implements a number guessing game where the user has to guess a randomly generated number within a specified range.

### Parameters
* `min_value` (int): The minimum value of the range (inclusive).
* `max_value` (int): The maximum value of the range (inclusive).

### Returns
* None. The game continues until the user guesses the number correctly.

### Game Rules
1. The user is prompted to guess a number within the specified range.
2. The user's guess is checked against the randomly generated number.
3. If the guess is too low, the user is informed and prompted to guess again.
4. If the guess is too high, the user is informed and prompted to guess again.
5. If the guess is correct, the user is congratulated and the game ends.

### Example Usage
```python
number_game(1,100) # Starts a new game with a number between 1 and 100
```

```python
import random

def number_game(min_value, max_value):
 """
 Implements a number guessing game where the user has to guess a randomly generated number within a specified range.

 Args:
 min_value (int): The minimum value of the range (inclusive).
 max_value (int): The maximum value of the range (inclusive).

 Returns:
 None. The game continues until the user guesses the number correctly.
 """
 number_to_guess = random.randint(min_value, max_value)
 attempts =0
 while True:
 user_guess = input(f'Guess a number between {min_value} and {max_value}: ')
 try:
 user_guess = int(user_guess)
 attempts +=1
 if user_guess < number_to_guess:
 print('Too low!')
 elif user_guess > number_to_guess:
 print('Too high!')
 else:
 print(f'Congratulations! You found the number in {attempts} attempts.')
 break
 except ValueError:
 print('Invalid input. Please enter a number.')

def main():
 number_game(1,100)

if __name__ == "__main__":
 main()
```