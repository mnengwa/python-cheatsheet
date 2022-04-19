# STRING LITERALS

> Resources: [Real Python](https://realpython.com)

## String variables

### Output & Input a string to the terminal

```python
# Output string to terminal
print("Welcome, what's your name?")

# Accept input from terminal & save it to variable
name = input()

# Use the input in the next output
print("Hello, " + name)
```

### Multi-line strings

```python
# Create a string with overfows to multiple lines
poem = """
Rose are red,
Skies are blue,
With great power comes great responsibility
"""

print(poem)
```

### Concatenate / combine many strings into one

```python
# placing two literal strings next to each other
print("Hi" + " " + "world")

# using the + operator
print("Hello, " "world")

# using join() method on a list of strings
print("".join(["Hey, ", "world"]))

# format() method
print('{} {} {}'.format("Morning", "good", "people"))

# %-formatting
print('%s %s %s' % ("Morning", "people", "of earth"))

# f-strings
# Python 3.6 & above ONLY
print(f'{"Hello"} {"earthlings"}')
```
