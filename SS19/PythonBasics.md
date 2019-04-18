
# Python Crash Course (Basics)


## Jupyther Notebook
Shortcuts:

| Shortcut    | Command                                              |
| ----------- | ---------------------------------------------------- |
| Shift+Tab   | Open Help                                            |
| Strg+Enter  | Run cell                                             |
| Shift+Enter | Run cell and select next cell                        |
| Alt+Enter   | Run cell and insert cell below                       |
| Strg+#      | Convert marked lines into comments (German Keyboard) |


## Datatypes
```python
integer = 1
floatingpoint = 2.5
complexnumber = 1 + 1j
string = 'abc'  # uses utf8
string2 = "abc"
string3 = '''abc'''  # Multiline comment
string4 = """abc"""
fstring = f"1 * 1 is {1*1}"
print(fstring)
```


## Arithmetic operations
```python
1 + 2
2 - 1
1 * 1
5 / 2
5 // 2
2 ** 2
```
Hint: integer has infinite numer of bits

## Collections
List
```python
l = [1, 'abc']
```
Tuple
```python
t = (1, 'abc')
```

Collection operations (Be carefull):

```python
print(l + l)
print(t * 3)
```

Indexing and slicing:
```python
l = list(range(10))
print(l[0])
print(l[-1])
print(l[::2])
print(l[1:6:2])
```
Start with 0. End with -1. Slice exclude last.

Dict:
```python
d = {'a': 1, 2: 'b'}  # d = dict(a=1)
print(d['a'], d[2])
```


## Conditions:

```python
a = 5
if a < 2:
    a = 2  # Note: indent instead of braces
elif not (a != 4) and (a <= 1000):
    a = 4
else:
    a = 6
```


## Loops:
```python
l = list(range(10))
for e in l:
    print(l)

while len(l) > 2:
    del l[2]
```


## List comprehensions:

```python
squares = [
    a ** 2
    for a in range(11)
    if a < 5
]
print(squares)
```


## Functions:

```python
def sub(a, b):
    """"Calculates a - b."""
    return a - b

print(sub(1, 2))
print(sub(b=2, a=1))
```


## Classes:
```python
class Dog:
    """Represents a dog."""
    def __init__(self, name):
        """Initialize dog object."""
        self.name = name
    def sit(self):
        """Simulate sitting."""
        print(self.name, 'is sitting')
```

## Task:

### Matirix Multiplication

Programm the multiplication of the matrices with `for` loops:
```python
A = [[1, 2], [3, 4]]
B = [[5, 6], [7, 8]]
C = ...
```

Python itself is not well suited for numeric problems.
Next lession: Numpy and Matplotlib.


## Advanced Topics

### Decorators
```python
# https://realpython.com/primer-on-python-decorators/#simple-decorators
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_whee():
    print("Whee!")

# Same as @my_decorator in front of say_whee
# say_whee = my_decorator(say_whee)
```


### Context manager
https://docs.python.org/3/library/contextlib.html

```python
with open('path/to/file') as fd:
    # to something with the file handle
```


### It is Easier to Ask for Forgiveness than Permission (EAFP)
https://en.wikipedia.org/wiki/Python_syntax_and_semantics#Exceptions


```python
try:
    ham = spam.eggs
except AttributeError:
    handle_error()
```


## Easter eggs

```python
from __future__ import braces
```

https://legacy.python.org/dev/peps/pep-0020/
```python
import this
```
