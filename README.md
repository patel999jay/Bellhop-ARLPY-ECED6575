# ECED6575
Bellhop Simulation

`Bellhop Python Simulation` relies on the following libraries:
```bash
- fortran compiler
- Arlpy
- Acoustic Toolbox
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

# Install latest `Acoustic Toolbox` (March 2019) 
Please make sure you have newer version of Bellhop.
```bash
cd ${HOME}/Documents
wget http://telecom.dei.unipd.it/ns/woss/files/at.zip
tar -xzf at.zip
cd at/at
make
sudo make install
```
Once installed, let's tell the system where to find our new libraries: (Please replace `ns` with your `hostname`
```bash
export PATH=/home/ns/Documents/at/at/Bellhop:/home/ns/Documents/at/at/:$PATH
```
