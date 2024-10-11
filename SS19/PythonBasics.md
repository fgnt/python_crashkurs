
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


# Motivation

Easy to learn, General Purpose Language, One of the most popular programming languages,
especially, for DNN, but also for signal processing and machine learning in general,
scripting language, i.e., no explicite compilation, high-level language, object oriented,
dynamic typing

# Basics


## Datatypes
```python
integer = 1
floatingpoint = 2.5
complexnumber = 1 + 1j
string = 'abc'  # uses utf8
string2 = "abc"  # no differnce between single and double quotes
string3 = '''abc'''  # Multiline comment
string4 = """abc"""
fstring = f"1 * 1 is {1*1}"
print(fstring)
```

Hint: No need for type declarations

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

In General:
 - `l[n]`: get n'th element
 - `l[s:e]`: get values from s to e, excluding e
   - Note: `l[:e] == l[0:e]` and `l[s:] == l[s:len(l)]`
 - ``

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


## Selection of Advanced Topics

### imports

Python has a large stdlib and an even bigger number of third party extensions (e.g., `numpy`).
```python
import functools, itertools
from pathlib import Path
```


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


### Exceptions: It is Easier to Ask for Forgiveness than Permission (EAFP)
https://en.wikipedia.org/wiki/Python_syntax_and_semantics#Exceptions


```python
try:
    ham = spam.eggs
except AttributeError:
    handle_error()
```


### Generators and iterators

Lazily generate sequences of values, useful for large datasets and infinite sequences

```python
def infinite_sequence(i=0):  # Generator
    while True:
        yield i
        yield from 'ab'
        i += 1
for r, i in zip(range(10), infinite_sequence(10)):
    print(r, i)
```

```python
class I:  # Iterator
    def __init__(self):
        self.i = 0
    def __iter__(self):
        return self
    def __next__(self):
        self.i += 1
        if self.i >= 10:
            raise StopIteration()
        return self.i

for i in I():
    print(i)
```
Recommendation: Don't use an iterator. There are very few cases,
where an implementation of `__iter__` and `__next__` is better
that a function with `yield`.

What the `for` loop does:
```python
it = iter(I())

while True:
    try:
        i = next(it)
    except StopIteration:
        break
    print(i)
```

### Type annotations

Intention: Code readability, IDE suppport and static type checker.
Note: They are ignored when you run the code.

```python
def div(a: int, b: int) -> float:
    c: float
    c = a / b
    d: float = a / b
    return c
```

### Assignment Expressions

Assign values to variables within an expression using the Walrus operator (`:=`).

```python
if (n := len(my_list)) > 5:
    print(f"List has {n} elements")
```

### Match-Case Statements

Structural pattern matching

```python
def http_status(status_code):
    match status_code:
        case 200 | 201:
            return "OK"
        case 400:
            return "Bad Request"
        case _:
            return "Unknown Status Code"

print(http_status(200))  # Output: OK
```


### Parallel

Search for `threading`, `multiprocessing` or `concurrent.futures`.

Note: The global interpreter lock (GIL) prevents python
to run python code in parallel, but at the same time
it makes python statement atomic and prevents many multithreading
issues known from other languages.

Note: Libs ĺike `numpy` release the GIL, while beeing in the C code
and hence the don't suffer from the GIL.


### Additional topics

 - async

## Easter eggs

```python
from __future__ import braces
```

https://legacy.python.org/dev/peps/pep-0020/
```python
import this
```
