# ECED6575 - Bellhop Simulation
--------------------------------------------------------------------------------------------------
### Author : Jay Patel

`Bellhop Python Simulation` relies on the following libraries:
```bash
- fortran compiler(optional)
- Acoustic Toolbox
- Windows Binaries
- Arlpy
- Python3
- Anaconda3(optional)
- Jupyter Notebook(optional)
```

Please check if you have python2 or python3 properly install in your windows 10. If you don't have them install in the machine, please refer [this link](https://www.python.org/downloads/).

Note : Make sure you download appropriate version of python for your machine. Most people will have [Win 10 x86-64 bit](https://www.python.org/ftp/python/3.8.3/python-3.8.3-amd64.exe), 
you can download other version from [this link](https://www.python.org/downloads/release/python-383/).

Make sure while installation ask you on first page about `Add python 3.8 to PATH` please tick mark that option, so it will automatically add into your windows env.

## Install [Acoustic Toolbox](http://oalib.hlsresearch.com/AcousticsToolbox/) 

- Download [AT Toolbox from this link](http://oalib.hlsresearch.com/AcousticsToolbox/at_2020_11_4.zip) : http://oalib.hlsresearch.com/AcousticsToolbox/at_2020_11_4.zip
- Also download binaries from the [same link](http://oalib.hlsresearch.com/AcousticsToolbox/atWin10_2020_11_4.zip).
- Extract the zip files to respective folders and put the binary files in to at folder. Also copy the folder path or remember where exactly you put them,
So your file structure should look like this:

* Local Folder Name
  * --\at\subfolders
  * --\atWin10_2020_6\binaries(*.exe files)
 
 - Now go to search bar and type `Edit the system environment variables` and click on the bottom of the box on `Environment Variables`, this will bring 
 another box and go to the down of section which says `system variables`, Select **Path** variable and click on `Edit...` and that will bring another dialogue box, please select `New` and put the exact same path in that box in which you put the above folders. Remember I told you to copy the folder path. then press ok. Also add those same paths to `user variables`
 - Also add binaries to the path, Here are three folders that was suppose to add to user and system path.
 
 ```bash
 C:\Users\Jay\Documents\bellhop
 C:\Users\Jay\Documents\bellhop\at
 C:\Users\Jay\Documents\bellhop\atWin10_2020_6
 ```
 
 For example i had extracted my files in the folder which is at `C:\Users\Jay\Documents\bellhop` then put the same path in the above box.
 - Directly go to normal command prompt of your system or choise of your terminal and install jupyter notebook.
 
 ## Install [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
 
    $ pip install --upgrade pip
    $ pip install jupyter
 
 - Now follow the steps mentioned in the `Install arlpy` section. 
 
 ## Anaconda (Optional)
 - This is recommanded as it will not messed up your python base enviornment. it comes with in build jupyter notebook capabilities.
 - Now Download and install [Anaconda](https://www.anaconda.com/products/individual) for better python enviornment handling. Basically we need jupyter notebook to visualize our simulation properly.(Recommended)
 - Download Python3.7 based 64 bit [installer](https://www.anaconda.com/products/individual) and install it.
 - Mark the option *Add Anaconda3 to the system PATH env*.
 - Open Anaconda Navigator from start menu. Go to Environments and `Create` new enviornment name `bellhop` and select `python 3.7`(you can select any python version above 3.4)
 - Install `numpy package` to `bellhop` environment, and then click on the play button and select `open terminal` and it will open a command prompt of your python virtual environment.
 
 you will see something like this,
 ```bash
 (bellhop) C:\Users\Jay>
 ```
 ## Install arlpy python package
 
    $ pip install arlpy
    
- This will install all necessary packages to your local virtual environment and You will see below message.
```bash
Successfully built arlpy utm bokeh
Installing collected packages: scipy, utm, python-dateutil, pytz, pandas, PyYAML, MarkupSafe, Jinja2, pillow, pyparsing, packaging, tornado, typing-extensions, bokeh, arlpy
Successfully installed Jinja2-2.11.2 MarkupSafe-1.1.1 PyYAML-5.3.1 arlpy-1.7.0 bokeh-2.1.1 packaging-20.4 pandas-1.0.5 pillow-7.1.2 pyparsing-2.4.7 python-dateutil-2.8.1 pytz-2020.1 scipy-1.5.0 tornado-6.0.4 typing-extensions-3.7.4.2 utm-0.5.0
```
[More Details](https://pypi.org/project/arlpy/)

- Now type `python` in the command prompt and try to `import arlpy`. If you get an error means your installation is broken.
```bash
(bellhop) C:\Users\Jay\Documents\bellhop\ECED6575\ECED6575-master\samplenotebook>python
Python 3.7.7 (default, May  6 2020, 11:45:54) [MSC v.1916 64 bit (AMD64)] :: Anaconda, Inc. on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import arlpy
>>>
```

Go the the folder where you have file name `bellhop.ipynb` using cd command,
i.e, 
    $ cd local-folder-path-for-bellhop.ipynb

### Usage - Running Jupyter notebook

Launch with:

    $ jupyter notebook
    
it will open up interactive python notebook into your default browser. Click on the file name `bellhop.ipynb` and it will bring up the sample notebook which shows you how to run the basic bellhop simulation. And command prompt output should look something like this.

```bash
(bellhop) C:\Users\Jay>cd C:\Users\Jay\Documents\bellhop\ECED6575\ECED6575-master\samplenotebook
(bellhop) C:\Users\Jay\Documents\bellhop\ECED6575\ECED6575-master\samplenotebook>jupyter notebook
[I 11:24:51.939 NotebookApp] JupyterLab extension loaded from C:\ProgramData\Anaconda3\lib\site-packages\jupyterlab
[I 11:24:51.939 NotebookApp] JupyterLab application directory is C:\ProgramData\Anaconda3\share\jupyter\lab
[I 11:24:51.970 NotebookApp] Serving notebooks from local directory: C:\Users\Jay\Documents\bellhop\ECED6575\ECED6575-master\samplenotebook
[I 11:24:51.970 NotebookApp] The Jupyter Notebook is running at:
[I 11:24:51.970 NotebookApp] http://localhost:8888/?token=b612cd2f264d2656d7bf8281efc0db592522b36af44caa14
[I 11:24:51.999 NotebookApp]  or http://127.0.0.1:8888/?token=b612cd2f264d2656d7bf8281efc0db592522b36af44caa14
[I 11:24:51.999 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 11:24:52.080 NotebookApp]

    To access the notebook, open this file in a browser:
        file:///C:/Users/Jay/AppData/Roaming/jupyter/runtime/nbserver-3500-open.html
    Or copy and paste one of these URLs:
        http://localhost:8888/?token=b612cd2f264d2656d7bf8281efc0db592522b36af44caa14
     or http://127.0.0.1:8888/?token=b612cd2f264d2656d7bf8281efc0db592522b36af44caa14
```

- This will open up notebook and you can go the `code` lines and press run button or press `Alt+Enter`, it will run the inline python code.

## Troubleshoot :

If you run `pm.models()` and it will return `[]` (I mean to say empty array.) means your bellhop is not in either system or user path. Please double chech that. 
```bash
[]
The `bellhop` model should be listed in the list of models above, if everything is good. If it isn't listed, it means that `bellhop.exe` is not available on the PATH, or it cannot be correctly executed. Ensure that `bellhop.exe` from the acoustics toolbox installation is on your PATH (updated `.profile` or equivalent, if necessary, to add it in).

From here on we assume that the `bellhop` model is available, and proceed...
```

If everything is ok and bellhop is correctly in your path then it will show you the following output.
```bash
['bellhop']
```
