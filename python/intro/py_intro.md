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
    Python has a convenient way to embed expressions inside string literals, using {}. This is called an f-string (formatted string literal).
    ```python
    name = "Alice"
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
- ## Data Type Convertion:
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
- # Arithmetic And Operations


  
  
