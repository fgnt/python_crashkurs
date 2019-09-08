# Use in Poolroom

Open a terminal and execute the following command:
```bash
source /upb/scratch/users/c/cbj/py37/bin/activate
```

(A backup anaconda is under `source /upb/users/l/ldrude/public/share/anaconda3/bin/activate`.)

This will setup anaconda in the current terminal.
Go to the directory where your excersises are (Use `cd <folder>` to change the directory and `ls` to show the content of the current directory).

Launch the jupyter server with the following command:
```bash
jupyter notebook
```

Complete example to run for the first time (i.e. initialize)
```bash
cd ~/
git clone https://git.cs.upb.de/chthiel/python-tutorial.git
cd ~/python-tutorial
source /upb/scratch/users/c/cbj/py37/bin/activate
jupyter notebook
```


Complete example to run if already initialized:
```bash
cd ~/python-tutorial
git pull  # Read the output and interpret if there is an error
source /upb/scratch/users/c/cbj/py37/bin/activate
jupyter notebook
```

# Use CoCalc
[https://cocalc.com/](https://cocalc.com/) Collaborative Calculation in the Cloud

 - Open a browser
 - Go to [https://cocalc.com/](https://cocalc.com/)
 - Log in
 - Open a project
 - Go to settings
 - Launch the Plain Jupyter server.

You can also use the build in Jupyter, but it misses some features.