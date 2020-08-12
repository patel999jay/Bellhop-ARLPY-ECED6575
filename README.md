# ECED6575 - Bellhop Simulation
--------------------------------------------------------------------------------------------------
### Author : Jay Patel, Dalhousie University, NS, Canada

`Bellhop Python Simulation` relies on the following libraries:
```bash
- fortran compiler
- Acoustic Toolbox
- Arlpy
- Python3
- Jupyter Notebook(optional)
```
* First make sure you have `gfortran`,`gcc` and `gcxx compiler`.

* Please checked if the GNU Fortran compiler was in my system by typing `gfortran --version`:
    ```bash
    GNU Fortran (Ubuntu 7.4.0-1ubuntu1~20.04.1) 7.4.0
    Copyright (C) 2017 Free Software Foundation, Inc.
    This is free software; see the source for copying conditions.  There is NO
    warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
    ```

If you have them then go for the GNU compiler, type:
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
If something goes wrong, you need to do `make clean` in order to clear all necessary files and then again run the above mentioned steps.

Once installed, let's tell the system where to find our new libraries: ( Please replace `ns` with your `hostname`)
```bash
export PATH=/home/ns/Documents/at/at/Bellhop:/home/ns/Documents/at/at/:$PATH
```
## Step 1. Install compilers and building tools

First let's check which Linux are you running with the command:
    
    lsb_release -ds
    
Will return something like:
    
    Debian GNU/Linux 9.8 (stretch)
    
* For *Debian/Ubuntu/Linux Mint*:
    
        $ sudo apt-get update
        $ sudo apt-get install wget nano gfortran m4 build-essential
    
* Also check your python version, it is recommanded to use python3.
   
        $ python --version
   
Will return something like:
    
         Python 2.7.18rc1
    
or you might have something like this if you have python3 correctly installed:
   
        $ python3 --version
   
Will return something like:
    
         Python 3.8.2
    

## Step 2. Install arlpy tools

Run the following command in your terminal. (It worked without sudo permission as well. It is recommanded to use sudo to installed everything properly.)

    $ pip3 install arlpy

or

    $ python3 -m pip install arlpy

or

    $ sudo -H pip3 install arlpy

#### OS Specific Installation
- [Windows 10](https://github.com/patel999jay/Bellhop-ARLPY-ECED6575/blob/master/Installation%20Manual_draft.pdf)
- [Mac OS](https://github.com/patel999jay/Bellhop-ARLPY-ECED6575/blob/master/MacOS%20Installation%20Manual.pdf)


[More Details](https://pypi.org/project/arlpy/)

## Step 3. Interactive IPython Notebooks - Jupyter Notebook (Optional)
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

You can find the example notebook of Bellhop in the repo folder named `sample notebook`. Follow the instruction and commands in the notebook to perform basic simulations with bellhop.

* If you want to see the notebook output figures then download `sample notebook/bellhop.html` and open in your browser, it will open up notebook with all the output graphs. 

## Troubleshoot

To chech you have correctly set your PATH for acoustic toolbox, please type this in your command prompt
    
    $ which bellhop.exe
   
It will show you path of your bellhop.exe, same like this,

    
    /home/ns/Documents/at/bin/bellhop.exe
    
 # Reference

  **1. M. Chitre 2020, “ARLPY python toolbox”** , https://github.com/org-arl/arlpy 
  
  **2. Ocean Acoustics Library.https://oalib-acoustics.org/**, Retrieved August 11, 2020.   
