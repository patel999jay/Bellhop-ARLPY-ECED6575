# ECED6575 - Bellhop Simulation
--------------------------------------------------------------------------------------------------
## Author : Jay Patel

`Bellhop Python Simulation` relies on the following libraries:
```bash
- fortran compiler
- Acoustic Toolbox
- Arlpy
- Python3
- Jupyter Notebook(optional)
```
First make sure you have `gfortran`,`gcc` and `gcxx compiler`.

Please checked if the GNU Fortran compiler was in my system by typing `gfortran --version`:
```bash
GNU Fortran (Ubuntu 7.4.0-1ubuntu1~18.04.1) 7.4.0
Copyright (C) 2017 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

If you go for the GNU compiler, type:
```bash
export FC=gfortran
```
`Acoustic Toolbox` is in repo folder named `AcousticToolbox`. You can download from there or follow the instruction below.

## Install latest `Acoustic Toolbox` (March 2019) 
Please make sure you have newer version of [Bellhop](https://oalib-acoustics.org/).
```bash
cd ${HOME}/Documents
wget http://telecom.dei.unipd.it/ns/woss/files/at.zip
tar -xzf at.zip
cd at/at
make
sudo make install
```

Once installed, let's tell the system where to find our new libraries: (Please replace `ns` with your `hostname`)
```bash
export PATH=/home/ns/Documents/at/at/Bellhop:/home/ns/Documents/at/at/:$PATH
```
## Step 1. Install compilers and building tools
First let's check which Linux are you running with the command:
```bash
lsb_release -ds
```
Will return something like:
```bash
Debian GNU/Linux 9.8 (stretch)
```
* For *Debian/Ubuntu/Linux Mint*:
```bash
sudo apt-get update
sudo apt-get install wget nano gfortran m4 build-essential
```
* Also check your python version, it is recommanded to use python3.
```bash
python --version
```
Will return something like:
```bash
Python 2.7.18rc1
```
or you might have something like this if you have python3 correctly installed:
```bash
python3 --version
```
Will return something like:
```bash
Python 3.8.2
```

## Step 2. Install arlpy tools
Run the following command in your terminal. (It worked without sudo permission as well. It is recommanded to use sudo to installed everything properly.)

`pip3 install arlpy`

or

`python3 -m pip install arlpy`

or

`sudo -H pip3 install arlpy`

[More Details](https://pypi.org/project/arlpy/)

## Steo 3. Interactive IPython Notebooks - Jupyter Notebook (Optional)
The Jupyter notebook is a web-based notebook environment for interactive computing.
### Installation
You can find the installation documentation for the
[Jupyter platform, on ReadTheDocs](https://jupyter.readthedocs.io/en/latest/install.html).
The documentation for advanced usage of Jupyter notebook can be found
[here](https://jupyter-notebook.readthedocs.io/en/latest/).

For a local installation, make sure you have
[pip installed](https://pip.readthedocs.io/en/stable/installing/) and run:

    $ pip install notebook

### Usage - Running Jupyter notebook

### Running in a local installation

Launch with:

    $ jupyter notebook

### Running in a remote installation

You need some configuration before starting Jupyter notebook remotely. See [Running a notebook server](https://jupyter-notebook.readthedocs.io/en/stable/public_server.html).

### Example Notebook of Bellhop

You can find the example notebook of Bellhop in the repo folder named `sample`. Follow the instruction and commands in the notebook to perform basic simulations with bellhop.

* If you want to see the notebook without then download `sample/bellhop.html` and open in your browser, it will open up notebook with all the output graphs. 

## Troubleshoot

To chech you have correctly set your PATH for acoustic toolbox, please type this in your command prompt
```bash
which bellhop.exe
```
It will show you path of your bellhop.exe, same like this,

```bash
/home/ns/Documents/at/bin/bellhop.exe
```
