# intern-CognoRise
# Define a function for each arithmetic operation
def add(x, y):
  return x + y

def subtract(x, y):
  return x - y

def multiply(x, y):
  return x * y

def divide(x, y):
  if y == 0:
    return "Error: Division by zero!"
  else:
    return x / y

# Main program
print("Simple Calculator")
print("----------------")

while True:
  # Get the first number from the user
  num1 = float(input("Enter the first number: "))

  # Get the operation from the user
  operation = input("Enter the operation (+, -, *, /): ")

  # Get the second number from the user
  num2 = float(input("Enter the second number: "))

  # Perform the calculation
  if operation == "+":
    result = add(num1, num2)
  elif operation == "-":
    result = subtract(num1, num2)
  elif operation == "*":
    result = multiply(num1, num2)
  elif operation == "/":
    result = divide(num1, num2)
  else:
    print("Invalid operation. Please try again!")
    continue

  # Display the result
  print(f"{num1} {operation} {num2} = {result}")

  # Ask if the user wants to continue
  response = input("Do you want to continue? (y/n): ")
  if response.lower() != "y":
    break

print("Goodbye!")
