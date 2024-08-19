# How to setup your Python environment for Data Analysis

This markdown takes you through the steps of setting up your environment.

## 1. Install Anaconda

Go to https://www.anaconda.com/download and provide email to download distribution.You will get the dwonload link vie email. 

Click the installer and go through the [istallation process](https://docs.anaconda.com/anaconda/install/windows/). 


## 2. Download Notepad++

It is a lightweight text editor which supports multiple file formats and programming languages with the appropriate formatting. (No code completion though.)


## 3. Get Windows Terminal

The easiest way to get it is from Microsoft Store; you can also go to https://learn.microsoft.com/en-us/windows/terminal/install for the package and the installation instructions.   

You may want to add Anaconda Prompt to your Windows Terminal. To do so, follow the instructions here: https://arturomoncadatorres.com/incorporating-anaconda-prompt-windows-terminal/


### 3a. Optional: Get Windows Subsystem for Linux

This is a Linux OS running on your Windows computer which enables you to develop cross-platform applications, improve your data science or web development workflows and 
manage IT infrastructure without leaving Windows.


## 4. Install git for Windows

Got to https://git-scm.com/download/win and install it from here.   

**Important!**: during the installation process select the `Use Visual Studio Code as Git's default editor` option when prompted for the default editor. Leave all other options as recommended by the installer. 
 

## 5. Get VS Code

It is one of the most widely used IDEs used in programming. The easiest way to to get it is from the Microsoft Store. Alternatively, you can download it from https://code.visualstudio.com/download.   

Once you have VS Code you need the following extensions (all can be installed from the IDE):

- Python (extension id: ms-python.python, link: https://marketplace.visualstudio.com/items?itemName=ms-python.python)

- Jupyter   
ms-toolsai.jupyter,  
Name: Jupyter   
Id: ms-toolsai.jupyter     
Description: Jupyter notebook support, interactive programming and computing that supports Intellisense, debugging and more.  
Version: 2024.6.0  
Publisher: Microsoft  
VS Marketplace Link: <https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter>
- markdownlint   
DavidAnson.vscode-markdownlint  
Name: markdownlint   
Id: DavidAnson.vscode-markdownlint   
Description: Markdown linting and style checking for Visual Studio Code   
Version: 0.55.0   
Publisher: David Anson   
VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint


## 6. Create a virtual environment for your data science course

A virtual environment is an isolated workspace for a particular project. In effect it is a directory structure which contains Python executable files and other files which tell Python the packages and their version numbers to use in that project. We set up this environment to make sure that we all get exactly the same results when running the code snippets. If you want ot take a deep dive into Python's virtual environment read [this](https://realpython.com/python-virtual-environments-a-primer/) detailed discussion of the topic. 

We are using `conda` to manage our environments and `pip` to download Python packages and to manage the dependencies between them. 

We also want to make sure that we are using a stable version of Python where all packages run fine. Users downloading Python to their laptops may have different versions, some of the working slightly differently than others. We can specify a certain Python version for each environment we use in various projects. For our project we are using Python 3.10. The following steps take you through the environment creation process. 

Type `Anadonda prompt` in the program search bar and open the application. This is a command line inteface, or CLI, with which you can interact with your Anaconda environment. This is the main environment where your Python code will run. 

Create a dedicated *virtual environment* by typing   

```bash
conda create --name myenv python=3.10
```
where '*myenv*' is the name of your dedicated virtual environment. You can call it *py310* to indicate the Python version you are using or *dataanalysis* to remind you on what you are using the virtual environment for, or whatever name you prefer. 