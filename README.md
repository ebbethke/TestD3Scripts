# TestD3Scripts
This python script sets up and runs a lightweight, threaded selenium browser session to allow CORS requests to make it easy to test web scripts from files on a local machine.

# Modules used/required to run
This tool was developed with Anaconda python 3.7, utilizing the following modules:
* http.server 
* selenium import webdriver
* socketserver
* threading
* os
* sys
* getopt

It also uses the following non-standard module:
* selenium=3.141.0=py37h4ab8f01_1001

# Installing from the provided .yml file
To make it easier to install and use, a YML anaconda environment file has been included.  To install, make sure anaconda for python 3+ is installed.
To install all the modules required (plus a few extras), from the anaconda environment call:
```conda env create --file meta.yml```
This will instruct anaconda to find and install all necessary modules to a standalone environment.

# Running the script
## Standalone from command line 
To run the script, from a compatible python environment, call the script with option ```-i``` then provide the path to the file from the command line.
You may provide any valid absolute filepath, e.g. ```"C:/Users/your_name/your_folder/some_file.html"```.  The script can also take any filename from the directory in which the file is being called from.

A full valid call might look like:
(meta) ... >> ```python browserserve.py -i "C:/Users/your_name/your_folder/some_file.html"```

You can also pass ```-h``` to print a simple help statement.

The script is setup to use selenium's Firefox drivers.  For more information about different python selenium webdrivers, see: (https://selenium-python.readthedocs.io/installation.html#drivers)[Selenium Python Web Drivers] 

## From Anaconda env
To run this from the provided anaconda environment, install the ```meta.yml``` env as above.  More info on anaconda envs here: (https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)[Anaconda: Managing Environments]  

To activate, from the anaconda prompt or similar call:
```conda activate meta```

You can now call the script as above.
