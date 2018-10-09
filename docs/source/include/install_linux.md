# Install for Linux

## Install
You can go to [https://www.anaconda.com/download/#linux](https://www.anaconda.com/download/#linux), download anaconda and execute the file (i.e. bash path/to/downloaded).

Or if you only want to use the commandline execute the following commands:

```bash
cd /path/to/install/anaconda  # e.g. cd /opt/

```
### Download anaconda and save it under `anaconda.sh`
```bash
wget https://repo.anaconda.com/archive/Anaconda3-5.2.0-Linux-x86_64.sh -O anaconda.sh
```

### Install anaconda. Answer all questions that get prompted
```bash
bash anaconda.sh
```
Alternative automatic install:
`bash anaconda.sh -b -p anaconda`.
For the arguments see [https://stackoverflow.com/a/28035048/5766934](https://stackoverflow.com/a/28035048/5766934) .

### Delete the downloaded installer (optional)
```bash
rm anaconda.sh
```

## Activate

Run the following to activate the new installed anaconda in the current shell:
```bash
source /path/to/install/anaconda/bin/activate

```
Alternative:
```bash
export PATH="/path/to/install/anaconda/bin:$PATH"
```
If you want to have the the new installed anaconda as default, add one of the above lines to your ~/.bashrc
