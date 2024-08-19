# How to setup your Python environment for Data Analysis

This markdown takes you through the steps of setting up your environment.

## 1. Install Anaconda

Go to https://www.anaconda.com/download and provide email to download distribution.You will get the dwonload link vie email. 

Click the installer and go through the [istallation process](https://docs.anaconda.com/anaconda/install/windows/). 


## 2. Download Notepad++

It is a lightweight text editor which supports multiple file formats and programming languages with the appropriate formatting. (No code completion though.)


## 3. Get Windows Terminal

`Windows Terminal` is a [command line interface](https://en.wikipedia.org/wiki/Command-line_interface) (`CLI`) application from Microsoft. Compared to Graphical User Interfaces (GUIs) these 'black windows' offer wider options to the experienced user to interact with applications, services, and system resources. At the beginning CLIs may look overwhelming but a little practice makes these interfaces more familiar. In many cases, running a command is much faster than opening a graphical user interface and then finding and clicking the appropriate drop-down menu to carry out a task. A CLI many times offers a wider range of customization options than GUIs.  

Windows Terminal is a modern host application for many command-line shells. The primary component windows are Command Prompt and PowerShell but, as we will see it below, other command-line applications can easily be integrated to Windows Terminal. The easiest way to get it is from Microsoft Store; you can also go to https://learn.microsoft.com/en-us/windows/terminal/install for the package and the installation instructions.   

Anaconda also offers a command line interface called `Anaconda Prompt`. We will use Anaconda Prompt during DA coding courses so you may want to add Anaconda Prompt to your Windows Terminal. To do so, follow the instructions here: https://arturomoncadatorres.com/incorporating-anaconda-prompt-windows-terminal/. This setup will make you a little more familiar with the neat tools a data scientist, or any computer professional, has at his or her disposal. 


### 3a. Optional: Get Windows Subsystem for Linux

This is a Linux OS running on your Windows computer which enables you to develop cross-platform applications, improve your data science or web development workflows and 
manage IT infrastructure without leaving Windows.


## 4. Install git for Windows and Register to GitHub

Got to https://git-scm.com/download/win and install it from here.   

**Important!**: during the installation process select the `Use Visual Studio Code as Git's default editor` option when prompted for the default editor. Leave all other options as recommended by the installer. 

Once you have installed git got to https://github.com/ and register and account. [GitHub](https://en.wikipedia.org/wiki/GitHub) is a developer platform that allows developers to create, store, manage and share their code. It has a wide range of services for companies and IT professionals. (You can even write and publish your [online books](https://www.gitbook.com/) with a related service.) GitHub is a payed service for those interested in its full capabilities but it is freely available for hosting, sharing and version-controlling computer codes. 

After registration open Windows Terminal (or Windows Powershell directly) and enter the following two commands using your username and and email address:
```bash
git config --global user.name "yourusername"
git config --global user.email youremail@example.com
```


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

To activate your virtual environment open an Anaconda Prompt windows (either from the Windows menu or by opening an Anaconda Promt windows from Windoes Terminal) and type 
```bash
conda activate myenv
```
where '*myenv*' is the name of your dedicated virtual environment.

To deactive your environment type
```bash
conda deactivate
```
When closing your Anaconda Prompt window, however, automatically deactivates your virtual environment. 

## 7. Open Jupyter Lab

Jupyter notebooks are your primary developent environment for writing and executing Python codes. (The name 'Jupyter' comes from 'Julia, Python, R'. Using the right environment, or 'kernel', Jupter notebooks can be used to run codes in these trhee languages.) The main feature of Jupyter notebooks is its interactive nature: you can check the interim results of your workflow, you can modify your existing codes and monitor how it works. 

To access your notebook open Anaconda prompt and type 
```bash
jupyter lab
```
After a few seconds your defult browser will be activated and in a separate window an url-like entry 'localhost:8888' will show. After this a notebook interface will be displayed. 