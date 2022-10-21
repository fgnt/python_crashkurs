
# Python Crash Course (Basics)

# The PEP 8 Song (PEP 8 -- Style Guide for Python Code)
https://www.youtube.com/watch?v=hgI0p1zf31k

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
Hint: integer has infinite numer of bits (e.g. `2**4000`)

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
l.append(3.2)
```

Indexing and slicing:
```python
l = list(range(10))
print(l[0])
print(l[-1])
print(l[::2])
print(l[1:6:2])
del l[3]
print(l)
l.append(3.2)
print(l)
```
Start with 0. End with -1. Slice exclude last.

Dict (Mapping, Hash):
```python
d = {'a': 1, 2: 'b'}  # d = dict(a=1)
print(d['a'], d[2])
print(d.keys())
print(d.values())
print(d.items())
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
    print(e)

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

squares = []
for a in range(11):
    if a < 5:
        squares.append(a ** 2)
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
A = [
    [1, 2, 3],
    [4, 5, 6],
]
B = [
    [7, 8],
    [9, 10],
    [11, 12],
]
C = ...   # [[58, 64], [139, 154]]
```

Optional question:
How many nested loops:
1:   ? 
2:   ?
3:   ? <-- correct
4:   ?

```
C = [[0,0],[0,0]]
for r in range(2):
    for c in range(2):
        for z in range(2):
            C[r][c] = C[r][c] + A[r][z]*B[z][c]        

C = [
    [
        sum(x*y for x, y in zip(a, b))
        for b in list(zip(*B))
    ]
    for a in A
]

```

Python itself is not well suited for numeric problems.
Next lession: Numpy

#### Preview for next week
```
import numpy as np
np.matmul(A, B)
```


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
