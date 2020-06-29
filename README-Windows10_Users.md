Please check if you have python2 or python3 properly install in your windows 10. If you don't have them install in the machine, please refer [this link](https://www.python.org/downloads/).

Note : Make sure you download appropriate version of python for your machine. Most people will have [Win 10 x86-64 bit](https://www.python.org/ftp/python/3.8.3/python-3.8.3-amd64.exe), 
you can download other version from [this link](https://www.python.org/downloads/release/python-383/).

Make sure while installation ask you on first page about `Add python 3.8 to PATH` please tick mark that option, so it will automatically add into your windows env.

## Install [Acoustic Toolbox](http://oalib.hlsresearch.com/AcousticsToolbox/) 

- Download [AT Toolbox from this link](http://oalib.hlsresearch.com/AcousticsToolbox/at.zip) : http://oalib.hlsresearch.com/AcousticsToolbox/at.zip
- Also download binaries from the [same link.](http://oalib.hlsresearch.com/AcousticsToolbox/)
- Extract the zip files to respective folders and put the binary files in to at folder. Also copy the folder path or remember where exactly you put them,
So your file structure should look like this:


* Local Folder Name
  * --\at\subfolders
  * --\atWin10_2020_6\binaries(*.exe files)
 
 
 - Now go to search bar and type `Edit the system environment variables` and click on the bottom of the box on `Environment Variables`, this will bring 
 another box and go to the down of section which says `system variables`, Select **Path** variable and click on `Edit...` and that will bring another dialogue box
 , please select `New` and put the exact same path in that box in which you put the above folders. Remember I told you to copy the folder path. then press ok.
 
 For example i had extracted my files in the folder which is at `C:\Users\Jay\Documents\bellhop` then put the same path in the above box.
 
 ## Anaconda 
 - Now Download and install [Anaconda](https://www.anaconda.com/products/individual) for better python enviornment handling. Basically we need jupyter notebook to visualize our simulation properly.(Recommanded)
 - Download Python3.7 based 64 bit [installer](https://www.anaconda.com/products/individual) and install it.
 - Don't mark the option *Add Anaconda3 to the system PATH env*.
 - Open Anaconda Navigator from start menu. Go to Environments and `Create` new enviornment name `bellhop` and select `python 3.7`(you can select any python version above 3.4)
 
