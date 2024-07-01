# Introduction to Python

Welcome to the Beginner Python Course! This course will introduce you to the basics of Python programming.

## Table of Contents

- [Introduction to Python](#introduction-to-python)
  - [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Installing Python](#installing-python)
- [Hello, World!](#hello-world)
- [Basic Syntax](#basic-syntax)
- [Variables and Data Types](#variables-and-data-types)
- [Arithmetic And Operations](#arithmetic-and-operations)
- [Iterable Data Structures](#iterable-data-structures)
- [Conditional Statements](#conditional-statements)
    - [if statements in Python are used to execute a block of code only if a certain condition is met.](#if-statements-in-python-are-used-to-execute-a-block-of-code-only-if-a-certain-condition-is-met)
- [Loops](#loops)
  - [Loops are fundamental constructs in Python that allow you to execute a block of code repeatedly.](#loops-are-fundamental-constructs-in-python-that-allow-you-to-execute-a-block-of-code-repeatedly)
  
# Introduction

Python is a high-level, interpreted programming language with a focus on readability and simplicity. It is widely used for web development, data analysis, artificial intelligence, and scientific computing.

# Installing Python

You can download Python from the official website 
- Through packages:
  
  - [for windows](https://www.python.org/downloads/windows/)

  - [for macOS](https://www.python.org/downloads/macos/)

  - [for Linux](https://www.python.org/downloads/source/)
  
Do not forget to add python to the path ([you can add it manually as well](https://phoenixnap.com/kb/add-python-to-path))

![Adding python to path](0_7nOyowsPsGI19pZT.png)

- Through the terminal :
  - For Linux:
    ```bash
    sudo apt update
    sudo apt install python3
    python3 --version
    ```
  - For macOS :
    ```bash
    brew update
    brew install python
    python3 --version
    ```





# Hello, World!

The first program we will write is the classic "Hello, World!" program. This program will simply print "Hello, World!" to the screen.

```python
print("Hello, BMGlab!")
```
# Basic Syntax
- ### comments:
  - Comments are used to annotate code with explanations or notes. They are ignored by the Python interpreter and are purely for human readers.
  
    We can create comments using # :
    ```python 
    print("I love tantuni")#this is a comment. I love tantuni by the way

- ### print :
    - The print command is the easiest way to send a specified message to the screen or other display device.
    This message or output can be a number, text, or the result of a calculation.

      ```python
      print(3)
      print(3+14)
      ```
    - Computers treat text and numbers differently. When printing text outputs, you need to enclose the text in either single or double quotes. This text is called a String: 
      ```python
      print("hello")
      print('world')
      ```
      Both the enclosing quotes need to be the same or else python will return an error. Run the code and see the results :
      ```python
      print("hello')
      ```
- ### input:
   - In Python, the input() function is used to accept user input from the keyboard 
        ```python
        # Converting input to integer
        age_str = input("Enter your age: ")
        age = int(age_str)

        # Converting input to float
        temperature_str = input("Enter the temperature: ")
        temperature = float(temperature_str)
        ``` 
# Variables and Data Types
- ## Basic Data types that you should know:
  - ### String : In Python, a string is a sequence of characters. It's used to store and manipulate text. Strings in Python are enclosed in either single quotes (') or double quotes (").

    ```python
    firstname = "Bond"
    lastname = 'James Bond'
    ```
    If you need a string that spans multiple lines, you can use triple quotes (''' or """):
    Example Code:
    ```python
    
    multiline_string1 = '''This is a
    multiline string.'''

    multiline_string2 = """This is also a
    multiline string."""
    ```
    Special Characters: 
    ```python
    print('One \nTwo \nThree')# use \n to create a new line
    print("\t hey \t there") #we can create a tab using \t: 
    ```



    Python has a convenient way to embed expressions inside string literals, using {}. This is called an f-string (formatted string literal).
    ```python
    name = "Efe"
    age = 30
    info = f"My name is {name} and I am {age} years old."
    print(info)  # "My name is Alice and I am 30 years old."

    ```
  - ### Int : In Python, integers are whole numbers without any decimal point. They can be positive or negative.'
    ```python
    my_number1 = 42

    my_number2 = -10
    ```
   - ### float : In Python, floats (floating-point numbers) are used to represent real numbers, including numbers with a decimal point or numbers expressed in scientific notation.
     ```python
     my_float1 = 3.14
     my_float2 = -0.5
     sci_float = 6.022e23  # 6.022 × 10^23
     ```
    - ### Boolean : Booleans are a data type that represents truth values. There are two boolean values: True and False. Booleans are used primarily for logical operations, comparisons, and flow control in programs.
      ```python
      is_active = True
      is_admin = False
      ```
- ## Declaration And Variables :
  - ### Variables : In Python, variables are used to store data values. They are assigned using the = operator. Here's how variables work:
    - Variable Declaration
        ```python
        # Assigning integer values to variables
            age = 25
            year = 2024

            # Assigning float values to variables
            pi = 3.14
            temperature = -10.5

            # Assigning string values to variables
            name = "Alice"
            message = 'Hello, World!'

            # Assigning boolean values to variables
            is_active = True
            is_admin = False
        ```
    - Variable Naming Rulse:
      - 1 - Variable names in Python can contain letters (both uppercase and lowercase), digits, and underscores (_).
      - 2 - Variable names cannot start with a digit.
      - 3 - Python keywords (like if, else, for, while, etc.) cannot be used as variable names.
      - 4 - Variable names are case-sensitive (age and Age are different variables).
  
  
    - Assigning Multiple Variables: You can assign values to multiple variables in a single line using commas.
        ```python
        x, y, z = 1, 2.0, "three"
        ```
    - Reassigning Variables : You can reassign a variable to a new value, regardless of its original type.
        ```python
        x = 10
        x = "Hello"
        ```
    - Python doesn't have built-in constant types like some other languages, but conventionally, constants are named in all uppercase letters.
        ```python
        PI = 3.14159
        MAX_VALUE = 100
        ```
- ## Data Type Conversion:
  - `str()` for strings:
    ```python
        num = 42
        num_str = str(num)  # Converts integer 42 to string '42'

        pi = 3.14
        pi_str = str(pi)  # Converts float 3.14 to string '3.14'

        is_active = True
        is_active_str = str(is_active)  # Converts boolean True to string 'True'
    ```
  - `int()` for integers:
    ```python
        # Converting from float to int
        num_float = 3.14
        num_int = int(num_float)  # 3

        # Converting from string to int
        num_str = "42"
        num_int = int(num_str)  # 42

        # Converting boolean to int
        is_active = True
        is_active_int = int(is_active)  # 1

    ```
    - `float()` for floats:
    ```python
        num = 42
        num_str = str(num)  # Converts integer 42 to string '42'

        pi = 3.14
        pi_str = str(pi)  # Converts float 3.14 to string '3.14'

        is_active = True
        is_active_str = str(is_active)  # Converts boolean True to string 'True'
    ```
    - `bool()` for boolean:
      - Integers and floats: Converts 0 to False and non-zero values to True.
      - Strings: Converts an empty string '' to False and non-empty strings to True.
      - None: Converts None to False.
    ```python
        # Converting from integer to boolean
        num_int = 0
        is_valid = bool(num_int)  # False

        # Converting from string to boolean
        str_value = "True"
        bool_value = bool(str_value)  # True (non-empty string is True)

        # Converting from float to boolean
        num_float = 3.14
        is_valid = bool(num_float)  # True (non-zero float is True)

    ```
  # Arithmetic And Operations
  - ## Basic Arithmetic Operators
    - 1. Addition (+)
       - Adds two numbers.
       - Can also concatenate strings.
       ```python
       # Numbers
        result = 5 + 3  # 8
        # Strings
        result = "Hello, " + "world!"  # "Hello, world!"
       ``` 
    - 2. Subtraction (-)
       - Subtracts the second number from the first. 
       ```python
       result = 5 - 3  # 2
       ``` 
    - 3. Multiplication (*)
        - Multiplies two numbers.
        - Repeats a string a specified number of times.
        ```python
        # Numbers
        result = 5 * 3  # 15

        # Strings
        result = "Hello! " * 3  # "Hello! Hello! Hello! "

        ``` 
    - 4. Division (/)
      - Divides the first number by the second, resulting in a float.
      ```python
      result = 5 / 2  # 2.5
      ``` 
    - 5. Floor Division (//)
      - Divides the first number by the second, rounding down to the nearest integer.
      ```python
      result = 5 // 2  # 2
      ``` 
    - 6. Modulus (%)
      - Returns the remainder of the division of the first number by the second.
      ```python
      result = 5 % 2  # 1
      ``` 
    - 7. Exponentiation (**)
      - Raises the first number to the power of the second.
      ```python
      result = 2 ** 3  # 8
      ``` 
    - 8. Arithmetic Boolean Operators
      - Booleans can be used in arithmetic operations, where True is treated as 1 and False as 0.
      ```python
      # Addition
      result = True + False  # 1 (1 + 0)

      # Subtraction
      result = True - False  # 1 (1 - 0)

      # Multiplication
      result = True * False  # 0 (1 * 0)

      # Division
      result = True / True  # 1.0 (1 / 1)
      ``` 
      ### Note:
    - Arithmetic operations between integers and floats follow the rules of arithmetic. When combining an integer and a float, the result is a float.
        ```python
        result = 5 // 2.0  # 2.0 (result is float because one operand is float)
        ``` 
  - ## Logical Operations
    - 1. AND (and)
      - The and operator returns True if both operands are True, otherwise it returns False.
      ```python
      # Both operands are True
      result = True and True  # True

      # One operand is False
      result = True and False  # False
      ``` 
    - 2. OR (or)
      - The or operator returns True if at least one operand is True, otherwise it returns False.
      ```python
      # Both operands are False
      result = False and False  # False

      # One operand is True
      result = True or False  # True
      ``` 
    - 3. NOT (not)
      - The not operator returns the opposite boolean value of its operand.
      ```python
      # Operand is True
      result = not True  # False

      # Operand is False
      result = not False  # True
      ``` 
    - 4. Equal to (==)
      - Checks if two values are equal.
      ```python
      result = 5 == 5  # True
      result = 5 == 3  # False
      result = "apple" == "apple"  # True
      ``` 
    - 5. Not equal to (!=)
      - Checks if two values are not equal.
      ```python
      result = 5 != 3  # True
      result = 5 != 5  # False
      result = "apple" != "Apple"  # True (case-sensitive)

      ``` 
    - 6. Greater/Less than (> , < ,<= , >=)
      - Compares the two values.
      ```python
      result = 5 > 3  # True
      result = 3 > 5  # False
      result = 3 < 5  # True
      result = 5 < 3  # False
      result = 5 <= 5 # True
      result = 5 >= 6 # False
      result = "apple" < "banana"  # True (based on Unicode values)
      a = 5
      result = 1 < a < 10  # True (equivalent to (1 < a) and (a < 10))

      b = 20
      result = a < b <= 20  # True (equivalent to (a < b) and (b <= 20))
      ```  
    - ### Truthy and Falsy Values: n Python, certain values are considered "truthy" (evaluated as True) and others are "falsy" (evaluated as False). Here's a summary:

      - Falsy values: None, False, 0 (numeric zero), 0.0 (float zero), '' (empty string), [] (empty list), () (empty tuple), {} (empty - dictionary), set() (empty set).
      - Truthy values: Any value that is not falsy.
      ```python
      result = 1 and 0  # False
      result = 1 and '1'#True
      ``` 

# Iterable Data Structures
  - ## Lists: Lists are one of the most commonly used data structures in Python. They are ordered, mutable (changeable), and can contain elements of different types.
    - Creating Lists: You can create a list by placing comma-separated values inside square brackets.
    ```python
    # Creating a list
    fruits = ["apple", "banana", "cherry"]
    numbers = [1, 2, 3, 4, 5]
    mixed = [1, "apple", 3.14, True]
    zeros = [0] * 5 # [0,0,0,0,0]

    # Empty list
    empty_list = []
    ``` 
    - Accessing Elements: You can access elements in a list using their index, with the first element having an index of 0.
    ```python
    fruits = ["apple", "banana", "cherry"]

    # Accessing elements
    first_fruit = fruits[0]  # "apple"
    second_fruit = fruits[1]  # "banana"

    # Negative indexing
    last_fruit = fruits[-1]  # "cherry"
    second_last_fruit = fruits[-2]  # "banana"
    ``` 
    - Slicing Lists: You can extract a part of a list (a slice) using the colon (:) operator.
    ```python
    numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

    # Slicing
    first_five = numbers[:5]  # [0, 1, 2, 3, 4]
    middle = numbers[3:7]  # [3, 4, 5, 6]
    last_three = numbers[-3:]  # [7, 8, 9]
    ``` 
    - Modifying Lists: You can modify elements in a list by assigning new values to specific indexes.
    ```python
    fruits = ["apple", "banana", "cherry"]

    # Modifying elements
    fruits[1] = "blueberry"
    print(fruits)  # ["apple", "blueberry", "cherry"]

    # Adding elements
    fruits.append("date")
    print(fruits)  # ["apple", "blueberry", "cherry", "date"]

    # Inserting elements
    fruits.insert(1, "banana")
    print(fruits)  # ["apple", "banana", "blueberry", "cherry", "date"]

    # Removing elements
    fruits.remove("blueberry")
    print(fruits)  # ["apple", "banana", "cherry", "date"]

    # Removing element by index
    del fruits[2]
    print(fruits)  # ["apple", "banana", "date"]

    # Popping elements
    last_fruit = fruits.pop()
    print(fruits)  # ["apple", "banana"]
    print(last_fruit)  # "date"
    ``` 
    - List Operations: You can perform various operations on lists, such as concatenation, repetition, and checking for membership.
    ```python
    list1 = [1, 2, 3]
    list2 = [4, 5, 6]

    # Concatenation
    combined = list1 + list2  # [1, 2, 3, 4, 5, 6]

    # Repetition
    repeated = list1 * 2  # [1, 2, 3, 1, 2, 3]

    # Membership
    is_in_list = 2 in list1  # True
    is_not_in_list = 7 not in list1  # True
    ``` 
    - ### Note: A strings can be treated like a list of characters
  - ## Tuples: Tuples are another essential data structure in Python. Unlike lists, tuples are immutable, meaning their elements cannot be changed after they are created.
    - Creating Tuples: You can create a tuple by placing comma-separated values inside parentheses.
    ```python
    # Creating a tuple
    fruits = ("apple", "banana", "cherry")
    numbers = (1, 2, 3, 4, 5)
    mixed = (1, "apple", 3.14, True)

    # Empty tuple
    empty_tuple = ()
    single_element_tuple = (1,) 
    ``` 
    - concatenation, repetition, slicing, accessing elements: Done exactly the same way with lists.
    ```python
    # Concatenation
    tuple1 = (1, 2, 3)
    tuple2 = (4, 5, 6)
    combined = tuple1 + tuple2  # (1, 2, 3, 4, 5, 6)

    # Repetition
    repeated = tuple1 * 2  # (1, 2, 3, 1, 2, 3)
    numbers = (0, 1, 2, 3, 4, 5, 6, 7, 8, 9)

    # Slicing
    first_five = numbers[:5]  # (0, 1, 2, 3, 4)
    middle = numbers[3:7]  # (3, 4, 5, 6)
    last_three = numbers[-3:]  # (7, 8, 9)
    fruits = ("apple", "banana", "cherry")

    # Accessing elements
    first_fruit = fruits[0]  # "apple"
    second_fruit = fruits[1]  # "banana"

    # Negative indexing
    last_fruit = fruits[-1]  # "cherry"
    second_last_fruit = fruits[-2]  # "banana"

    ``` 
    - Unpacking Tuples: You can unpack the elements of a tuple into variables.
    ```python
    fruits = ("apple", "banana", "cherry")

    # Unpacking
    first_fruit, second_fruit, third_fruit = fruits
    print(first_fruit)  # "apple"
    print(second_fruit)  # "banana"
    print(third_fruit)  # "cherry"

    ``` 
  - ## Sets: Sets are another important data structure in Python. They are unordered collections of unique elements, meaning they do not allow duplicate values.
    - Creating Sets: You can create a set by placing comma-separated values inside curly braces or by using the set() function.
    ```python
    # Creating a set
    fruits = {"apple", "banana", "cherry"}
    numbers = {1, 2, 3, 4, 5}
    mixed = {1, "apple", 3.14, True}

    # Empty set
    empty_set = set()

    # Note: Using {} creates an empty dictionary, not an empty set
    empty_dict = {}
    ``` 
    - Adding and Removing Elements: You can add elements to a set using the add() method and remove elements using the remove() or discard() methods.
    ```python
    fruits = {"apple", "banana", "cherry"}

    # Adding elements
    fruits.add("date")
    print(fruits)  # {"apple", "banana", "cherry", "date"}

    # Removing elements
    fruits.remove("banana")
    print(fruits)  # {"apple", "cherry", "date"}

    # Removing elements using discard (no error if the element does not exist)
    fruits.discard("banana")  # No error
    print(fruits)  # {"apple", "cherry", "date"}

    # Popping an element (removes and returns an arbitrary element)
    popped_element = fruits.pop()
    print(popped_element)  # An arbitrary element from the set
    print(fruits)  # Set with the remaining elements

    # Clearing the set
    fruits.clear()
    print(fruits)  # set()
    ``` 
    - Set Operations: Python sets support mathematical set operations such as union, intersection, difference, and symmetric difference.
    ```python
    set1 = {1, 2, 3, 4}
    set2 = {3, 4, 5, 6}

    # Union (elements in either set)
    union_set = set1.union(set2)  # {1, 2, 3, 4, 5, 6}
    # Alternatively
    union_set = set1 | set2  # {1, 2, 3, 4, 5, 6}

    # Intersection (elements in both sets)
    intersection_set = set1.intersection(set2)  # {3, 4}
    # Alternatively
    intersection_set = set1 & set2  # {3, 4}

    # Difference (elements in set1 but not in set2)
    difference_set = set1.difference(set2)  # {1, 2}
    # Alternatively
    difference_set = set1 - set2  # {1, 2}

    # Symmetric Difference (elements in either set but not in both)
    symmetric_difference_set = set1.symmetric_difference(set2)  # {1, 2, 5, 6}
    # Alternatively
    symmetric_difference_set = set1 ^ set2  # {1, 2, 5, 6}
    ```
  - ## Dictionaries: Dictionaries are another essential data structure in Python. They are unordered collections of key-value pairs, where each key is unique. 
    - Creating Dictionaries: You can create a dictionary by placing comma-separated key-value pairs inside curly braces, or by using the dict() function.
    ```python
    # Creating a dictionary
    fruits = {"apple": 1, "banana": 2, "cherry": 3}
    numbers = {1: "one", 2: "two", 3: "three"}
    mixed = {"name": "Alice", "age": 30, "is_student": True}

    # Empty dictionary
    empty_dict = {}

    # Using the dict() function
    another_dict = dict(name="Bob", age=25, is_student=False)
    ``` 
    - Accessing Elements: You can access elements in a dictionary by using their keys.
    ```python
    fruits = {"apple": 1, "banana": 2, "cherry": 3}

    # Accessing elements
    apple_count = fruits["apple"]  # 1
    banana_count = fruits["banana"]  # 2

    # Accessing non-existing key will raise a KeyError
    # mango_count = fruits["mango"]  # KeyError: 'mango'
    ``` 
    - Adding and Modifying Elements: You can add new key-value pairs or modify existing ones by assigning values to keys.
    ```python
    fruits = {"apple": 1, "banana": 2, "cherry": 3}

    # Adding a new key-value pair
    fruits["date"] = 4
    print(fruits)  # {"apple": 1, "banana": 2, "cherry": 3, "date": 4}

    # Modifying an existing key-value pair
    fruits["apple"] = 5
    print(fruits)  # {"apple": 5, "banana": 2, "cherry": 3, "date": 4}

    ``` 
    - Removing Elements: You can remove key-value pairs using the del statement or the pop() method.
    ```python
    fruits = {"apple": 1, "banana": 2, "cherry": 3, "date": 4}

    # Removing a key-value pair using del
    del fruits["banana"]
    print(fruits)  # {"apple": 1, "cherry": 3, "date": 4}

    # Removing a key-value pair using pop
    cherry_count = fruits.pop("cherry")
    print(fruits)  # {"apple": 1, "date": 4}
    print(cherry_count)  # 3

    # Removing all elements
    fruits.clear()
    print(fruits)  # {}

    ``` 
  - ## Type conversion 
    - `List()` for lists , `tuple()` for tuples , `set()` for sets and `dict()` for dictionaries. 
    ```python
        # List to tuple
    my_list = [1, 2, 3, 4]
    my_tuple = tuple(my_list)
    print(my_tuple)  # (1, 2, 3, 4)

        # Tuple to list
    my_tuple = (1, 2, 3, 4)
    my_list = list(my_tuple)
    print(my_list)  # [1, 2, 3, 4]

        # List to set
    my_list = [1, 2, 2, 3, 4, 4]
    my_set = set(my_list)
    print(my_set)  # {1, 2, 3, 4}

        # List of tuples to dictionary
    my_list = [("apple", 1), ("banana", 2), ("cherry", 3)]
    my_dict = dict(my_list)
    print(my_dict)  # {"apple": 1, "banana": 2, "cherry": 3}

    # List of lists to dictionary
    my_list = [["apple", 1], ["banana", 2], ["cherry", 3]]
    my_dict = dict(my_list)
    print(my_dict)  # {"apple": 1, "banana": 2, "cherry": 3}
    my_dict = {"apple": 1, "banana": 2, "cherry": 3}

    # Dictionary keys to list
    keys_list = list(my_dict.keys())
    print(keys_list)  # ["apple", "banana", "cherry"]

    # Dictionary values to list
    values_list = list(my_dict.values())
    print(values_list)  # [1, 2, 3]

    # Dictionary items to list of tuples
    items_list = list(my_dict.items())
    print(items_list)  # [("apple", 1), ("banana", 2), ("cherry", 3)]
    ``` 

# Conditional Statements
  ### if statements in Python are used to execute a block of code only if a certain condition is met.
  - Basic `if` Statement: An if statement evaluates a condition (which is an expression that returns True or False) and executes the indented block of code if the condition is True.
  ```python
  # Basic if statement
  x = 10
  if x > 5:
    print("x is greater than 5")  # This will be printed because 10 > 5
  ``` 
  - `if-else` Statement: You can use an else block to execute code when the if condition is False.
  ```python
  # if-else statement
  x = 3
  if x > 5:
      print("x is greater than 5")
  else:
      print("x is not greater than 5")  # This will be printed because 3 is not greater than 5
  ``` 
  - `if-elif-else` Statement: You can use multiple conditions with elif (short for "else if") to check additional conditions if the previous ones are False.
  ```python
  # if-elif-else statement
  x = 5
  if x > 5:
      print("x is greater than 5")
  elif x == 5:
      print("x is equal to 5")  # This will be printed because 5 == 5
  else:
      print("x is less than 5")
  ``` 
  - Nested if Statements: You can nest if statements to check conditions within other conditions.
  ```python
  # Nested if statements
  x = 10
  if x > 5:
      print("x is greater than 5")
      if x > 8:
          print("x is also greater than 8")  # This will be printed because 10 > 8
      else:
          print("x is not greater than 8")
  else:
      print("x is not greater than 5")
  ``` 
  - Using Logical Operators in if Statements: You can use logical operators (and, or, not) to combine multiple conditions.
  ```python
  # Using and operator
  x = 10
  if x > 5 and x < 15:
      print("x is between 5 and 15")  # This will be printed because both conditions are True

  # Using or operator
  y = 20
  if y < 10 or y > 15:
      print("y is either less than 10 or greater than 15")  # This will be printed because y > 15 is True

  # Using not operator
  z = 0
  if not z:
      print("z is 0 or False")  # This will be printed because not 0 is True
  ``` 
  - Checking for Membership: You can use the `in` and `not` in operators to check for membership in sequences like lists, tuples, and strings.
  ```python
  # Using in operator
  my_list = [1, 2, 3, 4, 5]
  if 3 in my_list:
      print("3 is in the list")  # This will be printed

  # Using not in operator
  my_string = "Hello, world!"
  if "Hello" not in my_string:
      print("Hello is not in the string")
  else:
      print("Hello is in the string")  # This will be printed
  ``` 

# Loops
## Loops are fundamental constructs in Python that allow you to execute a block of code repeatedly.
- ### For loops: A for loop is used to iterate over a sequence (such as a list, tuple, dictionary, set, ranges, or string).
```python
# Loop through a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
# Loop through a string
my_string = "Hello"
for char in my_string:
    print(char)
# Loop through a dictionary
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
for key, value in my_dict.items():
    print(f"{key}: {value}")

``` 




















 











 
   








 





 











 
 
     
  



 



 



 







 

 
   
 


 
 



 



 


 



  
  
