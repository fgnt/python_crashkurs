# Course Outline

This course is divided in three parts:

1. Installation, Jupyter and Python Basics
2. Numpy and Matplotlib
3. Pandas, Seaborn and Matplotlib

where the third part is for self studies.

## 0. Material
All material is available on github.

Go to https://github.com/fgnt/python_crashkurs to get the material (i.e. download https://github.com/fgnt/python_crashkurs/archive/master.zip) or better use git to clone the repository.
Windows users can download git from the official homepage (https://git-scm.com/downloads), and then use the `git` command from the `PowerShell`.
In Linux, git is already available in the `Terminal`.:
```
git clone https://github.com/fgnt/python_crashkurs.git
```

<!-- Note: The material is not finished. We will update it. -->

## 1. Installation and Python Basics
In this section we will set up your development environment and get familiar with very basic Python commands.
Please follow the Installation Manual for your OS: [Windows](./install_windows), [Linux](install_linux)
or follow the instruction at [Poolroom](poolroom.md) to start a jupyter notebook in the Poolroom.
Alternatively, you can use the [JupyterHub Server](ntcocalc.md) or external services like CoCalc (https://cocalc.com) or Colab (https://colab.research.google.com/).
<!-- Because of the remote teaching we use [CoCalc](./setup_ntcocalc). -->

### Material
1. Relevant Notebooks: [02_jupyter.ipynb][02_jupyter.ipynb], [03_python.ipynb][03_python.ipynb] (Catch-up Material)
2. Relevant CheatSheet: [beginners_python_cheat_sheet_pcc_all][beginners_python_cheat_sheet_pcc_all]

### Q: I didn't make it to the first lesson, what do I have to prepare for the next lesson?
1. Get a working enviroment, i.e. install anaconda on your private computer or figure out, how to activate anaconda in the poolroom.
2. Be able to launch a jupyter noteboook server
3. Clone https://github.com/fgnt/python_crashkurs to your computer.
4. Learn some python basics in a jupyter notebook. e.g. work through `notebooks/03_python.ipynb`

## 2 Numpy and Matplotlib
1. Introduction: [Numpy/SciPy](numpy)
2. Relevant CheatSheet: [Numpy_Python_Cheat_Sheet][Numpy_Python_Cheat_Sheet]
3. Relevant Exercises: [gertingold-numpy-tutorial-exercises.ipynb][gertingold-numpy-tutorial-exercises.ipynb], [math_to_code.ipynb][math_to_code.ipynb]

Note: For numpy we will spend two dates.

## 3. Pandas, Numpy, Scipy, Seaborn and Matplotlib (self studies)
Pandas is a very import package to manipulate and work with taublar data. In this section we will learn how to use the basic pandas datastructure called the `DataFrame`.

### Material
1. Relevant Notebooks: [05_matplotlib.ipynb][05_matplotlib.ipynb], [07_pandas.ipynb][07_pandas.ipynb], [07-01_pandas-apply.ipynb][07-01_pandas-apply.ipynb]
2. Relevant CheatSheet: [Pandas_Cheat_Sheet.pdf][Pandas_Cheat_Sheet.pdf]
3. Relevant Exercises Pandas: [03-01_Pandas_Task.ipynb][03-01_Pandas_Task.ipynb]
4. Relevant Exercises Numpy, Scipy and Plots: [03-02_Signal_Analysis_Task.ipynb][03-02_Signal_Analysis_Task.ipynb]


[03_python.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/notebooks/03_python.ipynb
[02_jupyter.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/notebooks/02_jupyter.ipynb
[beginners_python_cheat_sheet_pcc_all]: https://github.com/fgnt/python_crashkurs/tree/master/cheat_sheets/beginners_python_cheat_sheet_pcc_all.pdf
[Numpy_Python_Cheat_Sheet]: https://github.com/fgnt/python_crashkurs/tree/master/cheat_sheets/Numpy_Python_Cheat_Sheet.pdf
[Pandas_Cheat_Sheet.pdf]: https://github.com/fgnt/python_crashkurs/tree/master/cheat_sheets/Pandas_Cheat_Sheet.pdf

[gertingold-numpy-tutorial-exercises.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/WS2425/gertingold-numpy-tutorial-exercises.ipynb
[math_to_code.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/WS2425/math_to_code.ipynb


[05_matplotlib.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/notebooks/05_matplotlib.ipynb
[07_pandas.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/notebooks/07_pandas.ipynb
[07-01_pandas-apply.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/notebooks/07-01_pandas-apply.ipynb
[03-01_Pandas_Task.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/aufgaben/03-01_Pandas_Task.ipynb
[03-02_Signal_Analysis_Task.ipynb]: https://github.com/fgnt/python_crashkurs/tree/master/aufgaben/03-02_Signal_Analysis_Task.ipynb

