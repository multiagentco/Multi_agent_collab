

Development: Create a Python class Calculator with methods for basic arithmetic operations like addition, subtraction, multiplication, and division.
Testing: Write unit tests using Python's unittest framework to validate the Calculator class methods for various input scenarios.
Documentation: Generate documentation for the Calculator class, explaining its methods, parameters, and return values using Python docstrings.



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

### Parameters
* `operation` (str): The arithmetic operation to be performed. Supported operations are 'add', 'subtract', 'multiply', and 'divide'.
* `a` (int or float): The first operand.
* `b` (int or float): The second operand.

### Returns
* The result of the arithmetic operation if successful.
* 'Error: Division by zero' if division by zero is attempted.
* 'Error: Invalid operation' if an unsupported operation is provided.

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
```



Development: Create a Python class NumberGame with methods to generate a random number, check user input against the generated number, and provide hints or declare a win.
Testing: Write unit tests using Python's unittest framework to validate the NumberGame class methods for various input scenarios.
Documentation: Generate documentation for the NumberGame class, explaining its methods, parameters, and return values using Python docstrings.



```python
import random

class NumberGame:
 def __init__(self):
 self.number_to_guess = random.randint(1, 100)
 self.attempts = 0

 def check_guess(self, user_guess):
 self.attempts += 1
 if user_guess < self.number_to_guess:
 return 'Too low'
 elif user_guess > self.number_to_guess:
 return 'Too high'
 else:
 return f'Congratulations! You found the number in {self.attempts} attempts.'

def number_game():
 game = NumberGame()
 while True:
 try:
 user_guess = int(input('Guess a number between 1 and 100: '))
 result = game.check_guess(user_guess)
 print(result)
 if 'Congratulations' in result:
 break
 except ValueError:
 print('Invalid input. Please enter a number.')
```



```python
import unittest
from unittest.mock import patch
from your_module import NumberGame  # Replace 'your_module' with the actual module name

class TestNumberGame(unittest.TestCase):
 def test_check_guess_too_low(self):
 game = NumberGame()
 game.number_to_guess =5
 self.assertEqual(game.check_guess(3),'Too low')

 def test_check_guess_too_high(self):
 game = NumberGame()
 game.number_to_guess =5
 self.assertEqual(game.check_guess(7),'Too high')

 def test_check_guess_correct(self):
 game = NumberGame()
 game.number_to_guess =5
 self.assertEqual(game.check_guess(5),'Congratulations! You found the number in 1 attempts.')

if __name__ =='__main__':
 unittest.main()
```



## NumberGame Class Documentation
The `NumberGame` class implements a simple number guessing game.

### Methods
* `__init__`: Initializes a new game by generating a random number between 1 and 100, and setting the number of attempts to 0.
* `check_guess`: Checks if the user's guess is correct, too high, or too low, and returns a corresponding message. Increments the number of attempts.

### Example Usage
```python
game = NumberGame()
print(game.check_guess(50)) # Output: 'Too low', 'Too high', or 'Congratulations! You found the number in X attempts.'
```

## number_game Function Documentation
The `number_game` function runs the number guessing game.

### Behavior
* Creates a new `NumberGame` instance.
* Repeatedly asks the user for input until the correct number is guessed.
* Prints the result of each guess.

### Example Usage
```python
number_game() # Starts the number guessing game
```

```python
import random

class NumberGame:
 def __init__(self):
 self.number_to_guess = random.randint(1,100)
 self.attempts =0

 def check_guess(self, user_guess):
 self.attempts +=1
 if user_guess < self.number_to_guess:
 return 'Too low'
 elif user_guess > self.number_to_guess:
 return 'Too high'
 else:
 return f'Congratulations! You found the number in {self.attempts} attempts.'

def number_game():
 game = NumberGame()
 while True:
 try:
 user_guess = int(input('Guess a number between1 and100: '))
 result = game.check_guess(user_guess)
 print(result)
 if 'Congratulations' in result:
 break
 except ValueError:
 print('Invalid input. Please enter a number.')
```



```sql
SELECT c.customer_id, c.name, SUM(oi.quantity * oi.unit_price) AS total_spent
FROM customers c
JOIN orders o ON c.customer_id = o.customer_id
JOIN order_items oi ON o.order_id = oi.order_id
GROUP BY c.customer_id, c.name
ORDER BY total_spent DESC
LIMIT 3;
```



Development: Create a Python class NumberGame with methods to generate a random number within a specified range, check user input against the generated number, and provide hints or declare a win, along with tracking the number of attempts.
Testing: Write unit tests using Python's unittest framework to validate the NumberGame class methods for various input scenarios, including edge cases like invalid input or correct guesses on the first try.
Documentation: Generate documentation for the NumberGame class, explaining its methods, parameters, and return values using Python docstrings, and provide example usage in the module docstring.



```python
import random

class NumberGame:
 def __init__(self, min_value=1, max_value=100):
 self.number_to_guess = random.randint(min_value, max_value)
 self.attempts =0
 self.min_value = min_value
 self.max_value = max_value

 def check_guess(self, user_guess):
 if user_guess < self.min_value or user_guess > self.max_value:
 return f'Please guess a number between {self.min_value} and {self.max_value}.'
 self.attempts +=1
 if user_guess < self.number_to_guess:
 return 'Too low'
 elif user_guess > self.number_to_guess:
 return 'Too high'
 else:
 return f'Congratulations! You found the number in {self.attempts} attempts.'

def number_game(min_value=1, max_value=100):
 game = NumberGame(min_value, max_value)
 while True:
 try:
 user_guess = int(input(f'Guess a number between {min_value} and {max_value}: '))
 result = game.check_guess(user_guess)
 print(result)
 if 'Congratulations' in result:
 break
 except ValueError:
 print('Invalid input. Please enter a number.')
```



```python
import unittest
from your_module import NumberGame # Replace 'your_module' with the actual module name

class TestNumberGame(unittest.TestCase):
 def test_check_guess_out_of_range(self):
 game = NumberGame(1,10)
 self.assertEqual(game.check_guess(15),'Please guess a number between1 and10.')

 def test_check_guess_too_low(self):
 game = NumberGame(1,10)
 game.number_to_guess =5
 self.assertEqual(game.check_guess(3),'Too low')

 def test_check_guess_correct(self):
 game = NumberGame(1,10)
 game.number_to_guess =5
 self.assertEqual(game.check_guess(5),'Congratulations! You found the number in1 attempts.')

if __name__ =='__main__':
 unittest.main()
```



## NumberGame Class Documentation
The `NumberGame` class implements a simple number guessing game within a specified range.

### Methods
* `__init__`: Initializes a new game by generating a random number between `min_value` and `max_value` (default:1 and100), and setting the number of attempts to0.
* `check_guess`: Checks if the user's guess is within the valid range, and if so, checks if it's correct, too high, or too low, returning a corresponding message. Increments the number of attempts.

### Parameters
* `min_value` (int): The minimum value for the number to guess (default:1).
* `max_value` (int): The maximum value for the number to guess (default:100).

### Example Usage
```python
game = NumberGame(1,10)
print(game.check_guess(5)) # Output: 'Too low', 'Too high', or 'Congratulations! You found the number in X attempts.'
```

## number_game Function Documentation
The `number_game` function runs the number guessing game.

### Parameters
* `min_value` (int): The minimum value for the number to guess (default:1).
* `max_value` (int): The maximum value for the number to guess (default:100).

### Behavior
* Creates a new `NumberGame` instance with the specified range.
* Repeatedly asks the user for input until the correct number is guessed.
* Prints the result of each guess.

### Example Usage
```python
number_game(1,10) # Starts the number guessing game between1 and10
```

```python
import random

class NumberGame:
 def __init__(self, min_value=1, max_value=100):
 self.number_to_guess = random.randint(min_value, max_value)
 self.attempts =0
 self.min_value = min_value
 self.max_value = max_value

 def check_guess(self, user_guess):
 if user_guess < self.min_value or user_guess > self.max_value:
 return f'Please guess a number between {self.min_value} and {self.max_value}.'
 self.attempts +=1
 if user_guess < self.number_to_guess:
 return 'Too low'
 elif user_guess > self.number_to_guess:
 return 'Too high'
 else:
 return f'Congratulations! You found the number in {self.attempts} attempts.'

def number_game(min_value=1, max_value=100):
 game = NumberGame(min_value, max_value)
 while True:
 try:
 user_guess = int(input(f'Guess a number between {min_value} and {max_value}: '))
 result = game.check_guess(user_guess)
 print(result)
 if 'Congratulations' in result:
 break
 except ValueError:
 print('Invalid input. Please enter a number.')
```

