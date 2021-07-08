# Profiling

For profiling, we need here some wrapper code.
Since we wrote some wrapper code in our python toolbox (`paderbox`) to make it easy to use, you have to install the following to use it:

```bash
pip install paderbox line_profiler memory_profiler pycallgraph
```

in the Jupyter notebook you can use a `!` prefix in a cell to install them

```python
! pip install paderbox line_profiler memory_profiler pycallgraph
```

General comments:

 - When your think you code is slow, it is important to first figure out, where the code is slow.
 - When you profile your program, the profiler overhead may be critical, e.g. when you profile a loop which has only a few simple integer operations
 - Try to avoid loops in python. Using numpy with an independent axis is much faster (speedups above 100 aren't uncommon)

Now let me explain the `line_profiler` that I personally always use, to locate the bottleneck of my code.

First let us define a function, that we want to profile

```python
def fibonacci(n):
    value_old = 1
    value = 1
    for x in range(n):
        if x>1:
            temp = value
            value = value + value_old
            value_old = temp
        yield value
```

and another function that calls it

```python
from paderbox.utils.profiling import lprun
@lprun
def example_func():
    fib = 0
    for value in fibonacci(100):
        fib = value
    return fib
example_func()
```

The `@lprun` decorator marks this function, that we are interested in a profiling result of that function. Each time we now call this function, the profiling result will be printed (See later example, how it will look like).

If we are interested in the profiling result of the function `fibonacci` and not `example_func`, we can change the code to

```python
@lprun([fibonacci])
def example_func():
    fib = 0
    for value in fibonacci(100):
        fib = value
    return fib
example_func()
```

So now, we provide a list of intersted functions and classes to `lprun` and once we call `example_func`, we will get the profiling result for each function and each method of the classes.
Here an example output:

```
========== Profiling ==========
Timer unit: 1e-06 s

Total time: 0.000333 s
File: /home/ebbers/python_toolbox/nt/utils/profiling.py
Function: fibonacci at line 66

Line #      Hits         Time  Per Hit   % Time  Line Contents
==============================================================
    66                                               def fibonacci(n):
    67         1            2      2.0      0.6          value_old = 1
    68         1            1      1.0      0.3          value = 1
    69       101           56      0.6     16.8          for x in range(n):
    70       100           60      0.6     18.0              if x>1:
    71        98           53      0.5     15.9                  temp = value
    72        98           58      0.6     17.4                  value = value + value_old
    73        98           56      0.6     16.8                  value_old = temp
    74       100           47      0.5     14.1              yield value
```