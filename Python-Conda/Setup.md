# Conda

## Overview

Conda is an open source package management system and environment management system that runs on Windows, macOS and Linux.

[Conda Documentation](https://conda.io/docs/)

There are two types of conda:

* [Anaconda](https://conda.io/docs/glossary.html#anaconda-glossary)
* [Miniconda](https://conda.io/docs/glossary.html#miniconda)

## Download 

* [Anaconda Download](https://www.anaconda.com/download/)
* [Miniconda Download](https://conda.io/miniconda.html)

## Instatllation

* [Installation](https://conda.io/docs/user-guide/install/index.html)
* [Linux](https://conda.io/docs/user-guide/install/linux.html)
* [Windows](https://conda.io/docs/user-guide/install/windows.html#install-win-silent)


###Windows Notes

* Run downloaded executable
* Set path
	* conda path (e.g. C:\ProgramData\Miniconda3) 
	* conda scripts path (e.g. C:\ProgramData\Miniconda3\Scripts) 
* Create desktop short-cut
	* set it to default to Run as administrator if conda was installed for multiple users
	* set the default start directory to start in desire project folder

### Test Installation

* Run`conda list` to list installed components.  This also verifies the path is setup properly.
* Run`conda update conda`.  This verifies that Run as Administrator or permissions is setup properly is needed.

### Update

* Run`conda update conda`