# Installation for Linux

For a long time, anaconda was recommented. Since 2024, people searched for alterantives, because they changed the licensing terms.
As alternative, we show, how to install python with pyenv.

## Anaconda

Wikipedia:

> Anaconda is an open source data science and artificial intelligence distribution platform for Python and R programming languages.

While anaconda is convenient to be used, it changed in 2024 its licensing terms: It is no longer allowed to be used for free for research.

### Install
You can go to [https://www.anaconda.com/download/#linux](https://www.anaconda.com/download/#linux), download anaconda and execute the file (i.e. `bash path/to/downloaded`).

#### Pure installation from terminal
Or if you only want to use the commandline execute the following commands:

Go to the directory where you want to install anaconda
```bash
cd /path/to/install/anaconda  # e.g. cd /opt/

```

Download anaconda and save it under `anaconda.sh`
```bash
wget https://repo.anaconda.com/archive/Anaconda3-2024.02-1-Linux-x86_64.sh -O anaconda.sh
```

Install anaconda. Answer all questions that get prompted
```bash
bash anaconda.sh
```
Alternative automatic install:
`bash anaconda.sh -b -p anaconda`.
For the arguments see [https://stackoverflow.com/a/28035048/5766934](https://stackoverflow.com/a/28035048/5766934) .

Delete the downloaded installer (optional)
```bash
rm anaconda.sh
```

### Activate

Run the following to activate the new installed anaconda in the current shell:
```bash
source /path/to/install/anaconda/bin/activate
```
Alternative if you know what you are doing:
```bash
export PATH="/path/to/install/anaconda/bin:$PATH"
```
If you want to have the the new installed anaconda as default, add one of the above lines to your `~/.bashrc`. This will activate anaconda in all new shells (i.e. not in the ones that were opened befor this modifictaion).

## pyenv

An alternative installer to anaconda is [pyenv](https://github.com/pyenv/pyenv). They describe themself as 

> pyenv lets you easily switch between multiple versions of Python. It's simple, unobtrusive, and follows the UNIX tradition of single-purpose tools that do one thing well.

The instruction here, use pyenv only as convenient wrapper to install python, but ignores the switching, which has side effects for shared python installations and installations in network disks.

### Install

First, you have to install pyenv. The install folder is set with the environment variable `PYENV_ROOT`
and the installation is started, by executing a shell script:
```
export PYENV_ROOT="/opt/pyenv"
curl -fsSL https://pyenv.run | bash
```

You may have to install some build dependencies, on Ubuntu, you can run:
```
sudo apt update; sudo apt install build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev curl git libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
sudo apt  install cmake
```
see https://github.com/pyenv/pyenv/wiki#suggested-build-environment for other operating systems or the recent changes.
Note: Cmake is not listed as install dependency, but it is required for some third party packages (e.g., ToDO).

Next, you have to activate pyenv in your current shell
```
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init - bash)"
```
then you can list install candidates
```
pyenv install -l
```
and install python
```
pyenv install 3  # install recent py3
# pyenv install 3.12  # install recent py3.12
```

### Activate

To activate the environment, execute
```
export PATH="/opt/pyenv/versions/3.13.2/bin:$PATH"
```
or add the line to your `~/.bashrc`.
Note: You have to change the prefix and python version
to match your install location

### Third-party packages

In contrast to anaconda, the description here for pyenv installs only a minimal python
environment. So there are no third party packages installed.

Here, an example list of packages, that we installed for our exercises on the poolroom computers:
```
pip install jupyterlab notebook  # jupyter
pip install numpy scipy scikit-learn einops Cython pandas sympy numba numexpr dask pillow  # numeric
pip install matplotlib seaborn graphviz cycler  # plotting
pip install pytest autopep8 flake8 black pylint  # testing and code style
pip install fire click colorama termcolor platformdirs prompt-toolkit rich tabulate  # CLI
pip install soundfile requests PyYAML beautifulsoup4 dill diskcache h5py  # IO
pip install psutil tqdm natsort cached-property line_profiler humanfriendly
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install nbstripout

pip install tensorboard
pip install standard-imghdr  # tensorboard dependency
```

## Starting jupyter

Run the following command in a terminal, where anaconda is activated:
```bash
jupyter notebook
```

## Optional: IDE
Beside Jupyter Notebooks, there are various Integrated Development Environments Available (IDE) available for Python. While Spyder is a lightweight IDE that comes with Anaconda, we recommend using [Pycharm](https://www.jetbrains.com/pycharm/download/). You can even use Pycharm Professional for free after registering on the website with your university mail.
