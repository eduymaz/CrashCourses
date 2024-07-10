# Python String Manipulation

String manipulation is a fundamental skill in Python, allowing you to work with text data efficiently. Here are some common operations and methods for manipulating strings in Python:

## Creating Strings

You can create strings using single quotes, double quotes, or triple quotes (for multi-line strings).

```python
# Single quotes
string1 = 'Hello, World!'

# Double quotes
string2 = "Hello, World!"

# Triple quotes for multi-line strings
string3 = '''Hello,
World!'''
```
## Accessing Characters

You can access characters in a string using indexing. Python uses zero-based indexing.

```python
string = "Hello, World!"
print(string[0])  # Output: H
print(string[7])  # Output: W
```

## Slicing Strings

Slicing allows you to get a substring from a string.

```python
string = "Hello, World!"
print(string[0:5])  # Output: Hello
print(string[7:])   # Output: World!
print(string[:5])   # Output: Hello
print(string[-6:])  # Output: World!
```

## String Methods

Python provides many built-in methods for string manipulation:

### Changing Case

- `upper()`: Converts all characters to uppercase.
- `lower()`: Converts all characters to lowercase.
- `capitalize()`: Capitalizes the first character of the string.
- `title()`: Capitalizes the first character of each word.
- `swapcase()`: Swaps the case of all characters in the string.

```python
string = "Hello, World!"
print(string.upper())       # Output: HELLO, WORLD!
print(string.lower())       # Output: hello, world!
print(string.capitalize())  # Output: Hello, world!
print(string.title())       # Output: Hello, World!
print(string.swapcase())    # Output: hELLO, wORLD!
```
## Trimming Whitespace

- `strip()`: Removes leading and trailing whitespace.
- `lstrip()`: Removes leading whitespace.
- `rstrip()`: Removes trailing whitespace.

```python
string = "   Hello, World!   "
print(string.strip())  # Output: Hello, World!
print(string.lstrip()) # Output: Hello, World!   
print(string.rstrip()) # Output:    Hello, World!
```

## Replacing Substrings

- `replace(old, new)`: Replaces all occurrences of a substring with another substring.

```python
string = "Hello, World!"
print(string.replace("World", "Python"))  # Output: Hello, Python!
```

## Splitting and Joining

- `split(delimiter)`: Splits the string into a list of substrings based on a delimiter.
- `join(iterable)`: Joins a list of strings into a single string with a specified delimiter.

```python
string = "Hello, World!"
words = string.split(", ")
print(words)  # Output: ['Hello', 'World!']

delimiter = ", "
new_string = delimiter.join(words)
print(new_string)  # Output: Hello, World!
```
## Finding Substrings

- `find(substring)`: Returns the index of the first occurrence of a substring, or -1 if not found.
- `count(substring)`: Returns the number of non-overlapping occurrences of a substring.

```python
string = "Hello, World!"
print(string.find("World"))  # Output: 7
print(string.count("o"))     # Output: 2
```

## Checking Start and End

- `startswith(prefix)`: Checks if the string starts with the specified prefix.
- `endswith(suffix)`: Checks if the string ends with the specified suffix.

```python
string = "Hello, World!"
print(string.startswith("Hello"))  # Output: True
print(string.endswith("World!"))   # Output: True
```

## Formatting Strings

Python provides several ways to format strings:

- `format()`: Uses curly braces `{}` as placeholders for variables.
- f-strings (formatted string literals): Prefixed with `f`, allows embedding expressions inside string literals using `{}`.

```python
name = "Python"
version = 3.9

# Using format()
formatted_string = "Hello, {}. Version {}.".format(name, version)
print(formatted_string)  # Output: Hello, Python. Version 3.9.

# Using f-strings
formatted_string = f"Hello, {name}. Version {version}."
print(formatted_string)  # Output: Hello, Python. Version 3.9.
```

[Other methods regarding string Manipulation](https://www.w3schools.com/python/python_ref_string.asp)
