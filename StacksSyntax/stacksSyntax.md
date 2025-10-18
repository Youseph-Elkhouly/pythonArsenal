# Stack Implementation Guide for Python 3.9.6

## Table of Contents
1. [Basic Stack Class](#basic-stack-class)
2. [Key Stack Syntax Elements](#key-stack-syntax-elements)
3. [Core Operations](#core-operations)
4. [Error Handling](#error-handling)
5. [String Processing](#string-processing)
6. [Control Flow](#control-flow)
7. [Data Types and Literals](#data-types-and-literals)
8. [Operators](#operators)
9. [Functions and Methods](#functions-and-methods)
10. [Advanced Features](#advanced-features)

## Basic Stack Class

```python
class Stack:
    def __init__(self):
        self.items = []
    
    def push(self, item):
        self.items.append(item)
    
    def pop(self):
        if self.is_empty():
            raise IndexError("Cannot pop from an empty stack")
        return self.items.pop()
    
    def peek(self):
        if self.is_empty():
            raise IndexError("Cannot peek at an empty stack")
        return self.items[-1]
    
    def is_empty(self):
        return len(self.items) == 0
    
    def size(self):
        return len(self.items)
    
    def clear(self):
        self.items = []
    
    def contains(self, item):
        return item in self.items
    
    def get_all(self):
        return self.items.copy()
    
    def sort(self, key=None, reverse=False):
        """Sort the stack items in-place.
        
        Args:
            key: Optional function to extract comparison key from each item
            reverse: If True, sort in descending order (default: False)
        """
        self.items.sort(key=key, reverse=reverse)
    
    def __str__(self):
        return f"Stack({self.items})"
    
    def __repr__(self):
        return f"Stack({self.items})"
```

## Key Stack Syntax Elements

### Class Definition
```python
class Stack:
    def __init__(self):
        self.items = []
```

### Method Definitions
```python
def method_name(self, parameter):
    # method body
    return value
```

### List Operations for Stack
```python
self.items.append(item)    # Push to stack
self.items.pop()           # Pop from stack
self.items[-1]            # Peek at top
len(self.items)           # Get stack size
self.items == []          # Check if empty
self.items.clear()        # Clear stack
item in self.items        # Check if contains
self.items.copy()         # Get copy of stack
self.items.sort()         # Sort stack items
```

## Core Operations

### Error Handling
```python
if self.is_empty():
    raise IndexError("Error message")
```

### String Formatting
```python
f"Stack({self.items})"
```

### Conditional Statements
```python
if condition:
    # code block
elif condition:
    # code block
else:
    # code block
```

### Return Statements
```python
return value
return self.items.pop()
return len(self.items) == 0
```

### Method Calls
```python
stack.push(item)
stack.pop()
stack.peek()
stack.is_empty()
stack.size()
stack.sort()
```

### Variable Assignment
```python
stack = Stack()
result = stack.pop()
top_item = stack.peek()
```

### Loop Syntax
```python
while not stack.is_empty():
    item = stack.pop()
    print(item)
```

### Exception Handling
```python
try:
    result = stack.pop()
except IndexError as e:
    print(f"Error: {e}")
```

## String Processing

### String Methods for Token Processing
```python
token.isdigit()
token.startswith('-')
token[1:].isdigit()
```

### List Slicing
```python
token[1:]      # From index 1 to end
token[:5]      # From start to index 4
token[-1]      # Last character
```

### Type Conversion
```python
int(token)
str(value)
```

## Control Flow

### Comparison Operators
```python
==  # Equal
!=  # Not equal
>   # Greater than
<   # Less than
>=  # Greater than or equal
<=  # Less than or equal
```

### Logical Operators
```python
and  # Logical AND
or   # Logical OR
not  # Logical NOT
```

### Membership Operators
```python
in     # Check if item in container
not in # Check if item not in container
```

### Break/Continue
```python
break    # Exit loop
continue # Skip to next iteration
```

## Data Types and Literals

### String Literals
```python
"Double quotes"
'Single quotes'
f"f-string with {variable}"
```

### Numeric Literals
```python
42        # Integer
3.14      # Float
-123      # Negative number
```

### Boolean Literals
```python
True
False
```

### None
```python
None
```

### List Literals
```python
[]        # Empty list
[1, 2, 3] # List with items
```

## Operators

### Arithmetic Operators
```python
+  # Addition
-  # Subtraction
*  # Multiplication
/  # Division
// # Floor division
%  # Modulo
** # Exponentiation
```

### Assignment Operators
```python
=   # Assignment
+=  # Add and assign
-=  # Subtract and assign
*=  # Multiply and assign
/=  # Divide and assign
```

### Bitwise Operators
```python
&  # AND
|  # OR
^  # XOR
~  # NOT
<< # Left shift
>> # Right shift
```

### Augmented Assignment
```python
+=  # Add and assign
-=  # Subtract and assign
*=  # Multiply and assign
/=  # Divide and assign
//= # Floor divide and assign
%=  # Modulo and assign
**= # Exponentiate and assign
```

## Functions and Methods

### Function Definition
```python
def function_name(parameter1, parameter2):
    # function body
    return result
```

### Import Statements
```python
from module import class
import module
```

### Comments
```python
# Single line comment
"""
Multi-line comment
or docstring
"""
```

### Range
```python
range(10)        # 0 to 9
range(1, 11)     # 1 to 10
range(0, 10, 2)  # 0, 2, 4, 6, 8
```

### Enumerate
```python
for index, item in enumerate(items):
    # code
```

### Zip
```python
for item1, item2 in zip(list1, list2):
    # code
```

### List Comprehensions
```python
[item for item in items if condition]
[x for x in range(10)]
```

### Generator Expressions
```python
(item for item in items if condition)
```

### Lambda Functions
```python
lambda x: x * 2
```

### Map
```python
map(function, iterable)
```

### Filter
```python
filter(function, iterable)
```

### Sorted
```python
sorted(iterable)
sorted(iterable, key=function)
```

### Min/Max
```python
min(iterable)
max(iterable)
```

### Sum
```python
sum(iterable)
```

### Any/All
```python
any(iterable)
all(iterable)
```

### Len
```python
len(container)
```

### Type
```python
type(value)
isinstance(value, type)
```

### Print
```python
print(value)
print(f"Formatted {variable}")
print("Multiple", "values", sep=", ")
```

### Input
```python
user_input = input("Prompt: ")
```

## Advanced Features

### File Operations
```python
with open("file.txt", "r") as file:
    content = file.read()
```

### Context Managers
```python
with context_manager as variable:
    # code
```

### Assert
```python
assert condition, "Error message"
```

### Pass
```python
pass  # Do nothing
```

### Global
```python
global variable_name
```

### Nonlocal
```python
nonlocal variable_name
```

### Yield
```python
yield value
```

### Async/Await
```python
async def function():
    await other_function()
```

### Walrus Operator
```python
if (value := expression) > 0:
    # use value
```

### Dictionary Merging
```python
dict1 | dict2
```

## String Methods

### Basic String Methods
```python
string.upper()
string.lower()
string.strip()
string.split()
string.join()
string.replace()
string.find()
string.startswith()
string.endswith()
string.isdigit()
string.isalpha()
string.isalnum()
```

### Advanced String Methods
```python
string.capitalize()
string.casefold()
string.center()
string.count()
string.encode()
string.endswith()
string.expandtabs()
string.find()
string.format()
string.format_map()
string.index()
string.isalnum()
string.isalpha()
string.isascii()
string.isdecimal()
string.isdigit()
string.isidentifier()
string.islower()
string.isnumeric()
string.isprintable()
string.isspace()
string.istitle()
string.isupper()
string.join()
string.ljust()
string.lower()
string.lstrip()
string.maketrans()
string.partition()
string.replace()
string.rfind()
string.rindex()
string.rjust()
string.rpartition()
string.rsplit()
string.rstrip()
string.split()
string.splitlines()
string.startswith()
string.strip()
string.swapcase()
string.title()
string.translate()
string.upper()
string.zfill()
```

## List Methods

```python
list.append()
list.insert()
list.remove()
list.pop()
list.clear()
list.index()
list.count()
list.sort()
list.reverse()
list.extend()
list.copy()
```

## Set Methods

```python
set.add()
set.remove()
set.discard()
set.union()
set.intersection()
set.difference()
set.symmetric_difference()
set.clear()
set.copy()
set.difference_update()
set.intersection_update()
set.isdisjoint()
set.issubset()
set.issuperset()
set.symmetric_difference_update()
set.update()
```

## Dictionary Methods

```python
dict.get()
dict.setdefault()
dict.update()
dict.keys()
dict.values()
dict.items()
dict.pop()
dict.popitem()
dict.clear()
dict.copy()
dict.fromkeys()
```

## Tuple Methods

```python
tuple.count()
tuple.index()
```

## String Slicing

```python
string[start:end:step]
string[::2]      # Every 2nd character
string[::-1]     # Reverse
string[1:]       # From index 1 to end
string[:-1]      # From start to second last
```

## List Slicing

```python
list[start:end:step]
list[::2]        # Every 2nd item
list[::-1]       # Reverse
list[1:]         # From index 1 to end
list[:-1]        # From start to second last
```

## Unpacking

```python
a, b, c = [1, 2, 3]
*a, b = [1, 2, 3, 4]
```

## Multiple Assignment

```python
a, b = b, a  # Swap
a, b, c = 1, 2, 3
```

## Ternary Operator

```python
value = true_value if condition else false_value
```

## Chained Comparisons

```python
1 < x < 10
```

## Membership Testing

```python
item in container
item not in container
```

## Identity Testing

```python
a is b
a is not b
```

## Boolean Operators

```python
and  # Short-circuit AND
or   # Short-circuit OR
not  # Logical NOT
```

## String Concatenation

```python
"Hello" + " " + "World"
f"Hello {name}"
"Hello {}".format(name)
"Hello %s" % name
```

## String Formatting

```python
f"Value: {value}"
f"Value: {value:.2f}"
f"Value: {value:>10}"
f"Value: {value:<10}"
f"Value: {value:^10}"
```

## Escape Sequences

```python
\n  # Newline
\t  # Tab
\r  # Carriage return
\\  # Backslash
\"  # Double quote
\'  # Single quote
```

## Raw Strings

```python
r"C:\path\to\file"
```

## Bytes

```python
b"Hello"
```

## Unicode

```python
u"Hello"
```

## Raw Bytes

```python
rb"Hello"
```

## Formatted String Literals

```python
f"Value: {value}"
f"Value: {value!r}"
f"Value: {value!s}"
f"Value: {value!a}"
```

## Usage Examples

### Basic Stack Operations
```python
# Create stack
stack = Stack()

# Push items
stack.push(1)
stack.push(2)
stack.push(3)

# Check operations
print(stack.peek())    # 3
print(stack.size())    # 3
print(stack.is_empty()) # False

# Pop items
while not stack.is_empty():
    print(stack.pop())  # 3, 2, 1
```

### Stack Sorting Example
```python
# Create stack with unsorted items
stack = Stack()
stack.push(3)
stack.push(1)
stack.push(4)
stack.push(2)

print(f"Before sort: {stack}")  # Stack([3, 1, 4, 2])

# Sort the stack
stack.sort()
print(f"After sort: {stack}")   # Stack([1, 2, 3, 4])

# Sort in descending order
stack.sort(reverse=True)
print(f"Descending: {stack}")   # Stack([4, 3, 2, 1])

# Sort with custom key function
stack.push("apple")
stack.push("banana")
stack.push("cherry")
stack.sort(key=len)  # Sort by string length
print(f"By length: {stack}")   # Stack(['apple', 'banana', 'cherry'])
```

### Error Handling Example
```python
try:
    result = stack.pop()
    print(f"Popped: {result}")
except IndexError as e:
    print(f"Stack error: {e}")
```

### String Processing Example
```python
# Token processing for RPN
token = "-123"
if token.startswith('-') and token[1:].isdigit():
    value = int(token)
    stack.push(value)
```

## Notes

- This guide covers Python 3.9.6 syntax
- All examples are compatible with the current Python version
- Stack implementation uses list as underlying data structure
- Error handling is crucial for robust stack operations
- String slicing and processing are essential for token parsing
- Type conversion is important for mathematical operations

## License

This guide is provided for educational purposes in Data Structures and Algorithms learning.
