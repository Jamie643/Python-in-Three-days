# Day 3: Organizing Code and Beyond

Welcome to Day 3! Today, we'll learn how to organize our code into reusable blocks called functions, explore how to use pre-built code from modules, and get a brief introduction to file handling. We'll also discuss how these concepts relate to working with Large Language Models (LLMs).

## Functions

A *function* is a block of organized, reusable code that performs a specific task. Functions help to break down larger programs into smaller, more manageable pieces.  They also make your code more modular and easier to maintain.

Here's the basic syntax for defining a function in Python:

```python
def function_name(parameters):
    """Docstring:  A brief description of what the function does"""
    # Code to be executed inside the function
    # (Indented block)
    return result  # Optional:  Return a value
def: The keyword that indicates the start of a function definition.function_name:  A descriptive name for your function (e.g., calculate_area, greet_user).parameters:  Optional inputs that the function may take.  These are variables that the function will use. If a function doesn't need any input, the parentheses are empty: ().Docstring:  An optional, but highly recommended, string that explains what the function does.  It's enclosed in triple quotes ("""...""").Code block:  The indented block of code that the function executes.return:  An optional statement that specifies the value the function should send back to the caller.  If a function doesn't explicitly return a value, it implicitly returns None.Here's an example:def greet(person_name):
    """This function greets the person passed in as a parameter."""
    print(f"Hello, {person_name}!")

# Calling the function
greet("David")  # Output: Hello, David!

def add(num1, num2):
    """This function adds two numbers and returns the sum."""
    sum_result = num1 + num2
    return sum_result

# Calling the function and using the return value
result = add(7, 3)
print(f"The sum is: {result}")  # Output: The sum is: 10
Modules and LibrariesA module is a file containing Python code (functions, variables, etc.). A library is a collection of modules.  Python provides a rich set of built-in modules, and you can also install third-party libraries to extend Python's functionality.To use a module, you first need to import it using the import statement.import random  # Import the random module

# Using functions from the random module
random_number = random.randint(1, 10)  # Generate a random integer between 1 and 10
print(f"A random number between 1 and 10: {random_number}")

#Common Modules
import math #mathematical functions
print(math.pi)

import os #operating system interactions
print(os.getcwd())

import datetime #date and time
now = datetime.datetime.now()
print(now)
Introduction to File Handling (Brief)Python allows you to interact with files on your computer.  You can read data from files and write data to files.  This is often necessary when working with datasets, including text data for LLMs.Here's a basic example of reading from a file:try:
    with open("my_file.txt", "r") as file:
        content = file.read()
        print("Contents of my_file.txt:")
        print(content)
except FileNotFoundError:
    print("The file 'my_file.txt' was not found.")
Explanation:open("my_file.txt", "r"):  Opens the file named "my_file.txt" in read mode ("r").  The with statement ensures that the file is properly closed, even if errors occur.as file:  Assigns the opened file object to the variable file.file.read():  Reads the entire content of the file and returns it as a string.try...except:  This is a basic form of error handling.  If the file "my_file.txt" does not exist, a FileNotFoundError will be raised, and the code in the except block will be executed.Important: Before running this code, make sure you have a file named "my_file.txt" in the same directory as your Python script or notebook.  You can create this file with some text in it using a text editor.Looking Ahead: Relevance to LLMsThe concepts you've learned in this three-day crash course are fundamental to working with Large Language Models (LLMs):Strings: LLMs process and generate text, which is represented as strings in Python.Lists: Sequences of words or tokens are often stored in lists.Dictionaries: Vocabularies, mappings between words and their numerical representations (embeddings), and model parameters are often stored in dictionaries.Functions: You'll use functions to organize your code for training, evaluating, and using LLMs.Modules/Libraries: Libraries like TensorFlow, PyTorch, and Hugging Face Transformers provide the tools you need to build and work with LLMs.File Handling: You'll need to read and write text data from files to train and use LLMs.Day 3 Tasks:Function Fun:Write a function called calculate_area that takes the length and width of a rectangle as arguments and returns its area.Call this function with some sample values and print the result.# Your code for Task 1 here
Random Word Chooser:Create a list of your favorite words.Use the random module to randomly select and print one
