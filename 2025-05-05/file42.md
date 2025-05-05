Development: Create a Python class that represents a calculator with methods for basic arithmetic operations like addition, subtraction, multiplication, and division.
Testing: Write unit tests using Python's unittest framework to validate the calculator's functionality by checking the results of various operations.
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
``````python
assert calculator('add', 5, 3) == 8
assert calculator('divide', 10, 2) == 5.0
assert calculator('divide', 10, 0) == 'Error: Division by zero'
```## Calculator Function Documentation
The `calculator` function performs basic arithmetic operations on two numbers.

### Parameters
* `operation` (str): The operation to be performed. Can be 'add', 'subtract', 'multiply', or 'divide'.
* `a` (int or float): The first operand.
* `b` (int or float): The second operand.

### Returns
* The result of the operation if successful.
* 'Error: Division by zero' if division by zero is attempted.
* 'Error: Invalid operation' if an invalid operation is provided.

### Example Usage
```python
print(calculator('add', 5, 3))  # Output: 8
print(calculator('divide', 10, 2))  # Output: 5.0
print(calculator('divide', 10, 0))  # Output: 'Error: Division by zero'
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
```Development: Create a Python program that implements a simple number guessing game where the user has to guess a randomly generated number within a specified range.
Testing: Write unit tests using Python's unittest framework to validate the game's functionality, such as checking if the game correctly identifies a correct guess or handles invalid inputs.
Documentation: Generate documentation for the game using Python docstrings, explaining the rules, parameters, and return values of the game functions.```python
import random

def number_game(min_value, max_value):
 number_to_guess = random.randint(min_value, max_value)
 attempts = 0
 while True:
 try:
 guess = int(input(f'Guess a number between {min_value} and {max_value}: '))
 attempts += 1
 if guess < number_to_guess:
 print('Too low!')
 elif guess > number_to_guess:
 print('Too high!')
 else:
 print(f'Congratulations! You found the number in {attempts} attempts.')
 break
 except ValueError:
 print('Invalid input. Please enter a valid number.')
``````python
assert number_game(1,10) is None # This will not work as expected because number_game function does not return anything
# We need to refactor the code to make it testable

# Refactored code:
import random
import unittest
from unittest.mock import patch
from io import StringIO

def get_number_to_guess(min_value, max_value):
 return random.randint(min_value, max_value)

def check_guess(number_to_guess, guess):
 if guess < number_to_guess:
 return 'Too low!'
 elif guess > number_to_guess:
 return 'Too high!'
 else:
 return 'Congratulations! You found the number.'

class TestNumberGame(unittest.TestCase):

 @patch('sys.stdout', new_callable=StringIO)
 def test_get_number_to_guess(self, mock_stdout):
 self.assertGreaterEqual(get_number_to_guess(1,10),1)
 self.assertLessEqual(get_number_to_guess(1,10),10)

 def test_check_guess(self):
 self.assertEqual(check_guess(5,3),'Too low!')
 self.assertEqual(check_guess(5,7),'Too high!')
 self.assertEqual(check_guess(5,5),'Congratulations! You found the number.')

if __name__ =='__main__':
 unittest.main()
```## Number Game Function Documentation
The `number_game` function implements a simple number guessing game where the user has to guess a randomly generated number within a specified range.

### Parameters
* `min_value` (int): The minimum value of the range (inclusive).
* `max_value` (int): The maximum value of the range (inclusive).

### Returns
* None

### Gameplay
1. The function generates a random number between `min_value` and `max_value` (inclusive).
2. The user is prompted to guess the number.
3. After each guess, the function provides feedback in the form of "Too low!" or "Too high!".
4. The game continues until the user correctly guesses the number.
5. The function then prints a congratulatory message with the number of attempts taken.

### Example Usage
```python
number_game(1,10) # Starts a new game with a number between 1 and 10
```
```python
import random

def number_game(min_value, max_value):
 number_to_guess = random.randint(min_value, max_value)
 attempts =0
 while True:
 try:
 guess = int(input(f'Guess a number between {min_value} and {max_value}: '))
 attempts +=1
 if guess < number_to_guess:
 print('Too low!')
 elif guess > number_to_guess:
 print('Too high!')
 else:
 print(f'Congratulations! You found the number in {attempts} attempts.')
 break
 except ValueError:
 print('Invalid input. Please enter a valid number.')
```