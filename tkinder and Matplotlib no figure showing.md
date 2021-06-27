# tkinder and 'Matplotlib cannot show the figure' problem
tkinder is needed for matplotlib package to work properly.  
tkinder is included in Python3.x   
To get it automatcally, install Python from Windows Apps Store  

- Especially when you receive the warning when plotting figure with pyplot on an IDE like Pycharm or VS Code
> "UserWarning: Matplotlib is currently using agg, which is a non-GUI backend, so cannot show the figure.” 

## Solution
Change the configuration of matplotlib using the following:  
>import matplotlib  
matplotlib.use('TkAgg')  
import matplotlib.pyplot as plt

Possible issues after the change above
1. tkinter not found
>ModuleNotFoundError: No module named 'tkinter'  

- To install tkinter on Windows
`pip install python3-tk`  

- Try Use `import tkinter`  
Because pycharm already installed, see also [Install tkinter for Python](http://stackoverflow.com/questions/4783810/install-tkinter-for-python)

- To check if tkinder is available in the Python interpretor version, check by 
`python -m tkinter`  
Running python -m tkinter from the command line should open a window demonstrating a simple Tk interface, letting you know that tkinter is properly installed on your system, and also showing what version of Tcl/Tk is installed, so you can read the Tcl/Tk documentation specific to that version.

2. Other solution to plotting with matplotlib
>pip3 install PyQt5  
import matplotlib  
import matplotlib.pyplot as plt  
matplotlib.use('Qt5Agg')

3. If using Jupyter notebook try the following:
>%matplotlib inline

