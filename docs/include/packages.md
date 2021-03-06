# Installing and updating packages

Anaconda comes with a lot of scientific packages, however if you need an additional package or want to update one, you can use `conda` or `pip`.

## Update Anaconda Distribution

Anaconda publishes updates to its whole distribution every few months. Start _Anaconda Prompt_ (Windows) or activate the _Anaconda Enviroment_ (Linux) and update then by

```
conda update conda
conda update anaconda
```

## Installl new packages

Many packages are hosted on [Anaconda Cloud](https://anaconda.org/), you can search there for a package and follow the install instructions.

Typically you can install a new package with the following command inside _Anaconda Prompt_ (Windows) or the Terminal (Linux):

```
conda install -c conda-forge tensorflow
```
or
```
pip install tensorflow
```
We recommend to try conda first, especially if you are using windows. The conda command always delivers already compiled binaries. This is not guaranteed with pip.

## Conda vs pip

pip:
 - default python installer
 - has always up to date packages
 - usually maintained from the package owners
 - recommended for pure python packages

conda:
 - general purposed package manager
   - mainly used for python
 - some packages are outdated
 - recommended for libraries that have C++ dependencies (`numpy`, `scipy`, `matplotlib`, `cython`, `numba`, ...) 
   - These are well maintained from anaconda
   - numpy is usually faster when installed from conda
 - strongly recommended for windows users to avoid installing compilers 
