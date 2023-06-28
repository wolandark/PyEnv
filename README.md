# PyEnv
A shell script for quickly and easily making python virtual environments and installing python packages inside it in one go!

### Installation
Use curl to easily download the script to your home directory (or do it manually)
```
curl -O https://raw.githubusercontent.com/wolandark/PyEnv/master/PyVirtEnv
```
Make it executable
```
chmod +x PyVirtEnv
```

### Usage
Run the Script With $1 And If Needed, $2, $3 & $4 etc ...
Where $1 Is The First Argument And The New Virtual Env Name And $2 ... Is The Name Of An Optional Package/s To Be Installed With pip Into The Virtual Env
### [Example]: 
```
./PyVirtEnv NewEnv tinydb PyQt5
```
### [Setup]: 
Run The Script With The [setup] As Argument To Setup Your SHELL, SH & BASH Are Supported. Then source your .shellrc
### [Example]:
```
./PyVirtEnv setup
source ~/.bashrc
or
. ~/.shrc
```
This operation will simply echo a function to your .shellrc.
The function is:
```
PyEnv() { ~/PyVirtEnv "$@"; source "$1/bin/activate"; cd "$1"; }
```
With this configuration, you can call PyEnv from your terminal.
### [Example]:
```
PyEnv NewEnv tinydb PyQt5
```
### Why is it needed?
Because each shell script runs in its own subshell and therefore its impossible to automatically source the new env and cd into it from the script. However functions run with the shell itself so we can create the env, install packages and source the new env and cd into it in one go.
If this is not an issue for you, you can use the script normally and then source the new virtual environment and cd into it.
```
source <Env Name>/bin/activate
cd <Env Name>
```
For More Info Visit: https://docs.python.org/3/library/venv.html"
    
