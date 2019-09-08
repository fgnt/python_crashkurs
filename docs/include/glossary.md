# Glossary

### Python
Programming language

### CPython
Reference implementation

### Jupyter Notebook (ipython)
[https://jupyter.org/](https://jupyter.org/): The Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. Uses include: data cleaning and transformation, numerical simulation, statistical modeling, data visualization, machine learning, and much more.

## Common Libraries

### Buildin libraries

Path manypulation functions 
[`os.path`](https://docs.python.org/3/library/os.path.html)
or object-oriented filesystem paths.
[`pathlib`](https://docs.python.org/3/library/pathlib.html)
</br>
[`tempfile`](https://docs.python.org/3/library/tempfile.html)
e.g.: `tempfile.TemporaryDirectory`</br>
data serialization:
e.g.: [`json`](https://docs.python.org/3/library/json.html), [`pickle`](https://docs.python.org/3/library/pickle.html)</br>
[`itertools`](https://docs.python.org/3/library/itertools.html)
e.g.: `itertools.zip_longest`</br>
[`functools`](https://docs.python.org/3/library/functools.html)
e.g.: `functools.partial`</br>
[`collections`](https://docs.python.org/3/library/collections.html)
e.g.: `collections.defaultdict`, `collections.OrderedDict`</br>
[`contextlib`](https://docs.python.org/3/library/contextlib.html)
e.g.: `contextlib.contextmanager`</br>
Parallelization
[`concurrent.futures`](https://docs.python.org/3/library/concurrent.futures.html)
e.g.: `concurrent.futures.ThreadPoolExecutor`</br>
Shell commands
[`subprocess`](https://docs.python.org/3/library/subprocess.html)
e.g.: `subprocess.run`</br>
Pretty printer [`pprint`](https://docs.python.org/3/library/pprint.html),
alternative `IPython.lib.pretty.pprint`

And many more.

### Numpy/scipy 
Numpy (np) is the base library for numeric problems.
It contains the array datatype (np.ndarray) that is commonly used.
You can find there many math functions (`np.sum`, `np.einsum`, `np.linalg.norm`, `np.fft.fft`, ...).

### Plotting: Matplotlib/seaborn
Plotting librarys. Matplotlib is the base library for plots in python.
Additionally there are numerous libraries which focus on beatiful plots and easier handling which build upon matplotlib.
We generally recommend to use `seaborn` for special plots such as histograms, violinplots etc.

### Pandas
High-Perfomance Table style data representation

### Dask
Parallelisation of operations in DataFrames, Arrays or Lists

### Scikit-Learn (SK-Learn)
Machine Learning Library containing many popular methods in the areas of Classification, Regression, Clustering, Dimensionality Reduction, Model Selectioan and Preprocessing.

### Neural Networks
There are many Neural Networks Toolboxes available for python (SK-Learn beeing already one of them).
We generally recommend using TensorFlow or PyTorch.

### SymPy
Symbolic computations

### Sacred
Experiment configuration library (log configuration, stdout, ...) and command line interface:
`python -m path.to.experimentfile with parameter1=2`

### Pytest
Testing library
