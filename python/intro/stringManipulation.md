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