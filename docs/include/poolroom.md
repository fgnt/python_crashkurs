# Use in Poolroom

Open a terminal and execute the following command:
```bash
source /upb/scratch/users/c/cbj/py312/bin/activate
```

(Backup anaconda's are located at `source /upb/scratch/users/c/cbj/py39/bin/activate` and `source /upb/scratch/users/c/cbj/py37/bin/activate`.)

This will setup anaconda in the current terminal.
Go to the directory where your excersises are (Use `cd <folder>` to change the directory and `ls` to show the content of the current directory).

Launch the jupyter server with the following command:
```bash
jupyter notebook
```

Complete example to run for the first time (i.e. initialize)
```bash
cd ~/
git clone https://github.com/fgnt/python_crashkurs.git
cd ~/python_crashkurs
source /upb/scratch/users/c/cbj/py312/bin/activate
jupyter notebook
```


Complete example to run if already initialized:
```bash
cd ~/python-crashkurs
source /upb/scratch/users/c/cbj/py312/bin/activate
jupyter notebook
```

# JupyterHub

See [Remote: JupyterHub and alternatives](/include/ntcocalc)
