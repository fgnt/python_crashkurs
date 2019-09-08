# Installation for Linux

## Install
You can go to [https://www.anaconda.com/download/#linux](https://www.anaconda.com/download/#linux), download anaconda and execute the file (i.e. bash path/to/downloaded).

### Pure installation from terminal
Or if you only want to use the commandline execute the following commands:

Go to the directory where you want to install anaconda
```bash
cd /path/to/install/anaconda  # e.g. cd /opt/

```

Download anaconda and save it under `anaconda.sh`
```bash
wget https://repo.anaconda.com/archive/Anaconda3-5.3.0-Linux-x86_64.sh -O anaconda.sh
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

## Activate

Run the following to activate the new installed anaconda in the current shell:
```bash
source /path/to/install/anaconda/bin/activate

```
Alternative if you know what you are doing:
```bash
export PATH="/path/to/install/anaconda/bin:$PATH"
```
If you want to have the the new installed anaconda as default, add one of the above lines to your `~/.bashrc`. This will activate anaconda in all new shells (i.e. not in the ones that were opened befor this modifictaion).


## Starting jupyter

Run the following command in a terminal, where anaconda is activated:
```bash
jupyter notebooks
```

## Optional: IDE
Beside Jupyter Notebooks, there are various Integrated Development Environments Available (IDE) available for Python. While Spyder is a lightweight IDE that comes with Anaconda, we recommend using [Pycharm](https://www.jetbrains.com/pycharm/download/). You can even use Pycharm Professional for free after registering on the website with your university mail.