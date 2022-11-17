# FAQ for install issues

### Linux distribution and Windows with WSL

#### Install python

```{}
sudo apt update
sudo apt install python3.8 python3-pip
```

## Upgrade a package

```{}
pip install --upgrade <package-name>
```


## Create an environment

This can be useful in cases where you want to have a separate installation and avoid dependency issues.

```{}
sudo apt install python3.8-venv
python3 -m venv chip ## create the environment
source chip/bin/activate # activate the environment
deactivate # deactivate
```
