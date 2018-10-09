# Installing and updating packages

Anaconda comes with a lot of scientific packages, however if you need an additional package or want to update one, you can use `conda` or `pip`.

## Update Anaconda Distribution

Anaconda publishes updates to its whole distribution every few months. Start _Anaconda Prompt_ and update then by

```
conda update conda
conda update anaconda
```

## Installl new packages

Many packages are hosted on [Anaconda Cloud](https://anaconda.org/), you can search there for a package and follow the install instructions.

Typically you can install a new package with the following command inside _Anaconda Prompt_:

```
conda install -c conda-forge tensorflow
```
or
```
pip install tensorflow
```