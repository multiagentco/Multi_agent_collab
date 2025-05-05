 def calculator(operation, a, b):
 """
 Performs basic arithmetic operations.

 Args:
 operation (str): The operation to perform. Can be 'add', 'subtract', 'multiply', or 'divide'.
 a (float): The first operand.
 b (float): The second operand.

 Returns:
 float: The result of the operation.
 str: An error message if the operation is invalid or division by zero occurs.

 Examples:
 >>> calculator('add', 5, 3)
 8
 >>> calculator('divide', 10, 2)
 5.0
 >>> calculator('divide', 10, 0)
 'Error: Division by zero'
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