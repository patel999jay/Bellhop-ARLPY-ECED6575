# ECED6575 - Bellhop Simulation

##### Author : Jay Patel, Dalhousie University, NS, Canada
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)](https://github.com/ellerbrock/open-source-badges/)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)


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

|Sr No.| Link | DESCRIPTION |
| ------| ------ | ------ |
|1.| [Bellhop Simulation](https://patel999jay.github.io/post/bellhop-acoustic-toolbox/) | Bellhop - Ray Tracing |
|2.| [Bellhop Sample Notebook](https://github.com/patel999jay/Bellhop-ARLPY-ECED6575/blob/master/samplenotebook/bellhop.ipynb) | Bellhop Sample Notebook |
|3.| [Bellhop another usecase Notebook](https://github.com/patel999jay/Bellhop-ARLPY-ECED6575/blob/master/samplenotebook/SampleNotebookBellhop2021.ipynb) | Bellhop another usecase Notebook [(PDF)](https://github.com/patel999jay/Bellhop-ARLPY-ECED6575/blob/master/samplenotebook/SampleNotebookBellhop2021%20-%20Jupyter%20Notebook.pdf) |
|4.| [Bellhop Introduction](https://github.com/patel999jay/Bellhop-ARLPY-ECED6575/blob/master/samplenotebook/Bellhop_Introduction_2021.ipynb) | Bellhop Introduction [(PDF)](https://github.com/patel999jay/Bellhop-ARLPY-ECED6575/blob/master/samplenotebook/Bellhop_Introduction_2021.pdf) |
|5.| [Simple plotting GUI Tool for ARLPY](https://github.com/patel999jay/arlpy_gui) | Simple plotting GUI Tool for ARLPY |

## Install latest `Acoustic Toolbox` (Dec 2024) 

### Note ⚠️
**Important:** This is a critical instruction from [Ocean Acoustics Library - OALIB](https://oalib-acoustics.org/). **Look at the compile dates carefully!**

    at source code (zip file) for Mac, Linux, or Windows. Binaries are *NOT* provided. (2024_12_25) ; you need to build this. You can use the above commands to build this. 
    at Binaries (zip file) for Windows 10. This version is older than the one above. (The source code is also included so that you can access the compatible Matlab routines that read/write model input/output.) *(2020_11_4)*

    The Fortran2008 source code should be fully portable. The Windows10 binaries were compiled for a plain vanilla Intel architecture. Therefore they will likely be slower that one that you compile yourself for the native architecture.


#### 1. instruction for Linux-base machines
Please make sure you have newer version of [Bellhop](https://oalib-acoustics.org/).
```bash
cd ${HOME}/Documents
wget http://oalib.hlsresearch.com/AcousticsToolbox/at_2024_12_25.zip
unzip at_2024_12_25.zip
cd at
make clean
make all
sudo make install
sudo ldconfig
```
If something goes wrong, you need to do `make clean` in order to clear all necessary files and then again run the above mentioned steps.

### Note ⚠️
**Important:** Please make proper changes in the `at/MakeFile` about PC/the system architecture details correctly. You may need to specify an architecture flag under gfortran:
```
-mcpu=apple-m2 ( for M2 processor)
-mcpu=ARMv8.6-A ( for generic ARM processor instruction sets)
```
For the **Linux** : Make sure you have this line uncommented:
```
# This is for Linux
export FFLAGS= -march=native -Bstatic -Waliasing -Wampersand              -Wintrinsics-std -Wno-tabs -Wintrinsic-shadow -Wline-truncation         -std=gnu  -O1 -ffast-math -funroll-all-loops -fomit-frame-pointer -mtune=native
# This is for Mac
# export FFLAGS= -mcpu=apple-m2 -Bstatic -Waliasing -Wampersand              -Wintrinsics-std -Wno-tabs -Wintrinsic-shadow -Wline-truncation         -std=gnu  -O1 -ffast-math -funroll-all-loops -fomit-frame-pointer
```
For more details, checkout this issue -- **gfortran doesn't work**: [https://github.com/patel999jay/Bellhop-ARLPY-ECED6575/issues/3]


Once installed, let's tell the system where to find our new libraries: ( Please replace `ns` with your `hostname`)
```bash
export PATH=/home/ns/Documents/at/at/Bellhop:/home/ns/Documents/at/at/:$PATH
```

#### 2. instruction for Windows-based machines
Please download the binary files from the [Bellhop](https://oalib-acoustics.org/). You can find them on this [page](http://oalib.hlsresearch.com/AcousticsToolbox/) -- [Here](http://oalib.hlsresearch.com/AcousticsToolbox/atWin10_2020_11_4.zip).

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

### Simple plotting GUI for ARLPY

You can find this cool small GUI tool [here](https://github.com/patel999jay/arlpy_gui).

## Troubleshoot

To chech you have correctly set your PATH for acoustic toolbox, please type this in your command prompt
    
    $ which bellhop.exe
   
It will show you path of your bellhop.exe, same like this,

    
    /home/ns/Documents/at/bin/bellhop.exe
    
 # Reference

  **1. M. Chitre 2020, “ARLPY python toolbox”** , https://github.com/org-arl/arlpy 
  
  **2. Ocean Acoustics Library.** https://oalib-acoustics.org/, Retrieved August 11, 2020.   
  
  **3. Jay Patel and Mae Seto,** Underwater channel characterization for shallow water multi-domain communications, Proceedings of Meetings on Acoustics 40, 070014 (2020),
https://doi.org/10.1121/2.0001316, Retrieved July 07, 2021.
