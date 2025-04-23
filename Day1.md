# Day 1: Python Fundamentals

Welcome to Day 1 of your Python crash course! Today, we'll cover the very basics of Python programming.

## Introduction to Python

Python is a versatile and easy-to-learn programming language. It's widely used in many areas, including web development, data science, and, importantly for our purposes, Artificial Intelligence (AI) and Machine Learning (ML).

* **Why Python for AI/ML?** Python's simple syntax makes it easy to write and read code.  It also has a rich ecosystem of libraries (collections of pre-written code) that are very helpful for AI/ML, such as NumPy, pandas, and scikit-learn.

## Variables and Data Types

In Python, we use *variables* to store data. Think of a variable as a named container that holds a value.  Every value in Python has a *data type*. Here are some fundamental data types:

* **Integer (`int`):** Whole numbers (e.g., -3, 0, 10, 1000).
* **Float (`float`):** Decimal numbers (e.g., 3.14, -0.5, 2.0).
* **String (`str`):** Text enclosed in single quotes ('hello') or double quotes ("world").
* **Boolean (`bool`):** Represents truth values: `True` or `False`.

Here's how you can create variables and assign values to them:

```python
# Assigning values to variables
name = "Alice"  # String
age = 30      # Integer
height = 1.75  # Float
is_student = False # Boolean

# Printing the values of the variables
print("Variables and their values:")
print(f"Name: {name}")
print(f"Age: {age}")
print(f"Height: {height}")
print(f"Is student: {is_student}")
The f before the opening quote in the print statement allows us to embed the variable values directly into the string.  This is called an "f-string".OperatorsOperators are symbols that perform operations on values. Let's look at some common ones:Arithmetic Operators: Used for mathematical calculations.+ (Addition)- (Subtraction)* (Multiplication)/ (Division)// (Floor Division - divides and rounds down to the nearest integer)% (Modulo - returns the remainder of a division)** (Exponentiation)Comparison Operators: Used to compare values. They return either True or False.== (Equal to)!= (Not equal to)> (Greater than)< (Less than)>= (Greater than or equal to)<= (Less than or equal to)Logical Operators: Used to combine or modify boolean values.and (Returns True if both operands are True)or  (Returns True if at least one operand is True)not (Negates a boolean value)Here are some examples:# Arithmetic Operators
num1 = 10
num2 = 5

print("Arithmetic Operators:")
print(f"{num1} + {num2} = {num1 + num2}")
print(f"{num1} - {num2} = {num1 - num2}")
print(f"{num1} * {num2} = {num1 * num2}")
print(f"{num1} / {num2} = {num1 / num2}")
print(f"{num1} // {num2} = {num1 // num2}")
print(f"{num1} % {num2} = {num1 % num2}")
print(f"{num1} ** {num2} = {num1 ** num2}")

# Comparison Operators
print("\nComparison Operators:")
print(f"{num1} > {num2}: {num1 > num2}")
print(f"{num1} < {num2}: {num1 < num2}")
print(f"{num1} == {num2}: {num1 == num2}")

# Logical Operators
x = True
y = False
print("\nLogical Operators:")
print(f"x and y: {x and y}")
print(f"x or y: {x or y}")
print(f"not x: {not x}")
Basic Input and OutputWe can use Python to get input from the user and display output.print() function: Used to display output to the console.input() function: Used to get input from the user.  The input() function displays a prompt to the user and then waits for them to type something and press Enter.  The function then returns what the user typed as a string.# Output using print()
print("Hello, World!")
print("Welcome to Python!")

# Input using input()
city = input("What city do you live in? ")
print(f"You live in {city}.")

name = input("What is your name? ")
print(f"Nice to meet you, {name}!")
Important Note for Google Colab (and some other online environments): The input() function might not work exactly as expected in some online environments.  If you encounter a StdinNotImplementedError, you can temporarily replace the input() function with a direct assignment, like this:#  For Colab (if you get an error)
# city = "Your City Here"
# name = "Your Name Here"
Remember to replace "Your City Here" and "Your Name Here" with actual values.  When you run Python locally, the input() function will work correctly.Control Flow - If StatementsIf statements allow us to make decisions in our code.  They let us execute different blocks of code depending on whether a condition is True or False.The basic syntax of an if statement is:if condition:
    # Code to execute if the condition is True
    # (Indented block)
elif another_condition:  # Optional
    # Code to execute if another_condition is True
    # (Indented block)
else:  # Optional
    # Code to execute if none of the conditions are True
    # (Indented block)
if:  The first condition to check.elif (short for "else if"):  An optional additional condition to check if the first condition is False.  You can have multiple elif blocks.else:  An optional block of code to execute if none of the preceding if or elif conditions are True.Here's an example:temperature = 25

if temperature > 30:
    print("It's very hot!")
elif temperature > 20:
    print("It's a warm day.")
elif temperature > 10:
    print("It's a mild day.")
else:
    print("It's a cold day.")
Day 1 Tasks:Now it's your turn to write some Python code!Greeting Enhancer:Modify the "Hello, World!" program from the beginning of this day.Ask the user for their name using the input() function.Then, print a personalized greeting that includes their name.For example, if the user enters "Bob", the output should be "Hello, Bob!".# Your code for Task 1 here
Simple Calculator:Write a program that takes two numbers as input from the user.You can either get input separately, or on the same line.Print the sum, difference, product, and quotient of the two numbers.If the second number is zero, print a message saying that division by zero is not allowed.# Your code for Task 2 here
