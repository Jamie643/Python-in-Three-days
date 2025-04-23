# Day 2: Data Structures and Repetition

Welcome to Day 2! Today, we'll learn how to organize data using data structures and how to automate repetitive tasks using loops.

## Data Structures - Lists and Tuples

*Data structures* are ways of organizing and storing data.  Lists and tuples are two fundamental data structures in Python used to store collections of items.

### Lists

A *list* is an ordered collection of items. Lists are:

* **Ordered:** The items in a list have a specific order, and that order is preserved.
* **Mutable:** You can change the contents of a list after it's created (you can add, remove, or modify items).
* **Created with square brackets `[]`:**

    ```python
    # Creating a list of fruits
    fruits = ["apple", "banana", "cherry"]

    # Accessing elements by index (starting from 0)
    print(fruits[0])  # Output: apple
    print(fruits[1])  # Output: banana

    # Modifying a list
    fruits.append("orange")  # Add "orange" to the end
    print(fruits)  # Output: ['apple', 'banana', 'cherry', 'orange']
    fruits[1] = "grape"       # Change the second item
    print(fruits)
    fruits.remove("cherry")
    print(fruits)

    #Other methods
    #Insert
    fruits.insert(1, "kiwi")  #inserts "kiwi" at index 1
    print(fruits)
    #Extend
    more_fruits = ["mango", "pineapple"]
    fruits.extend(more_fruits) #adds all elements from more_fruits
    print(fruits)

    #Removing elements
    #Remove
    fruits.remove("banana") #removes first occurence of "banana"
    print(fruits)

    #Pop
    removed_fruit = fruits.pop(1) #removes and returns element at index 1
    print(removed_fruit)
    print(fruits)

    #Clear
    #fruits.clear() #removes all elements from the list
    #print(fruits)
    ```

### Tuples

A *tuple* is also an ordered collection of items, similar to a list. However, tuples are:

* **Ordered:** Like lists, the order of items is preserved.
* **Immutable:** You cannot change the contents of a tuple after it's created.  This means you can't add, remove, or modify items.
* **Created with parentheses `()`:**

    ```python
    # Creating a tuple of colors
    colors = ("red", "green", "blue")

    # Accessing elements by index
    print(colors[0])  # Output: red
    print(colors[2])  # Output: blue

    # You can't modify a tuple!  The following would cause an error:
    # colors.append("yellow")  # Error!
    # colors[0] = "purple"    # Error!

    #Tuple packing and unpacking
    my_tuple = 1, "hello", 3.4 #tuple packing
    print(my_tuple)

    a, b, c = my_tuple # tuple unpacking
    print(a,b,c)
    ```

**Key Difference:** Lists are mutable (changeable), while tuples are immutable (unchangeable).  Use lists when you need a collection of items that might change, and use tuples when you have a collection of items that should remain fixed.

## Data Structures - Dictionaries

A *dictionary* is a different kind of data structure that stores data in *key-value* pairs.  Think of it like a real-world dictionary where you look up a word (the *key*) to find its definition (the *value*).

* **Key-Value Pairs:** Each item in a dictionary consists of a key and its associated value.
* **Keys must be unique:** You can't have duplicate keys in a dictionary.
* **Values can be of any data type:** The values can be strings, numbers, lists, or even other dictionaries.
* **Created with curly braces `{}`:**

    ```python
    # Creating a dictionary to store student information
    student = {
        "name": "Charlie",
        "age": 20,
        "major": "Computer Science",
        "city": "New York"
    }

    # Accessing values using keys
    print(student["name"])  # Output: Charlie
    print(student["age"])   # Output: 20

    # Adding a new key-value pair
    student["university"] = "NYU"
    print(student)
    #Modifying
    student["age"] = 21
    print(student)

    #Removing
    del student["city"]
    print(student)

    #Other methods
    #Get
    print(student.get("name")) #returns value of name
    print(student.get("grade", "Not Available")) #returns "Not Available" if "grade" key does not exist

    #Keys, Values, Items
    print(student.keys()) #returns a view object of keys
    print(student.values()) #returns a view object of values
    print(student.items()) #returns a view object of key-value pairs (tuples)

    #Copy
    student_copy = student.copy() #returns a shallow copy
    print(student_copy)

    #Update
    student.update({"age": 22, "year": "Senior"}) #updates age and adds year
    print(student)
    ```

## Loops - For Loops

*Loops* are used to execute a block of code repeatedly.  A *for loop* is used to iterate over a sequence (like a list, tuple, or string).

```python
# Iterating over a list
fruits = ["apple", "banana", "cherry"]
print("Iterating over a list using a for loop:")
for fruit in fruits:
    print(f"I like {fruit}.")

# Iterating over a string
print("\nIterating over a string using a for loop:")
for char in "Python":
    print(char)

#Using range
print("\nIterating using range():")
for i in range(5): #generates numbers from 0 to 4
  print(i)

for i in range(2, 6): #generates numbers from 2 to 5
  print(i)

for i in range(0, 10, 2): #generates even numbers from 0 to 8
  print(i)
Loops - While LoopsA while loop repeatedly executes a block of code as long as a condition is True.count = 0
print("\nUsing a while loop:")
while count < 5:
    print(f"Count is: {count}")
    count += 1  # Important:  This line updates the count, otherwise the loop would continue forever!

#Using break and continue
print("\nUsing break and continue:")
for i in range(10):
  if i == 3:
    continue #skip iteration
  print(i)
  if i == 5:
    break #exit loop
Day 2 Tasks:List Analyzer:Create a program that takes a list of numbers.Print the largest number, the smallest number, and the average of the numbers in the list.# Your code for Task 1 here
Dictionary Fun:Create a dictionary representing a simple inventory of items (e.g., {"apple": 10, "banana": 25, "orange": 15}).Write a program that allows you to enter an item name.Print the quantity of that item in the inventory.If the item is not found, print a message saying so.# Your code for Task 2 here
