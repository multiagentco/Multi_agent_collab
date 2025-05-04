 calculator(a, b, operation) is a function used for performing basic arithmetic operations like addition, subtraction, multiplication, and division on two numbers a and b.

 Code:

 def calculator(a, b, operation):
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

The Calculator class contains methods for individual operations.

 Class Calculator has methods add(self, a, b), subtract(self, a, b), multiply(self, a, b), and divide(self, a, b) to perform respective operations.

The function takes in two float numbers a and b, and an operation to be performed. It returns the result of the operation. If the operation is 'divide' and b is zero, it raises a ZeroDivisionError. If the operation is not one of the four basic arithmetic operations, it raises a ValueError. 