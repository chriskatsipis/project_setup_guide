# Basic guide on how to initiate a python project in vscode

#### Step1: Folder
We create a folder for the project, then open said folder in vscode

#### Step2: Files
We create a new python file  inside the folder using vscode with `File>New File...`

#### Step3: Venv
We want to create a venv for this project. A venv allows for installation of libraries inside the project, not affecting the system as a whole
##### 3.1: Open a cmd terminal in vscode by navigating the the terminal panel (located at the bottom of the window) and clicking on the arrow next to the (+) sign, then selecting cmd
##### 3.2: Locate the installation of python in your system by running `where python`
##### 3.3: Now type `-m venv`, and a name for the venv (i use the default venv) at the end of your python location and run it to create the venv `C:\Users\User\AppData\Local\Python\Python312\python.exe -m venv venvname"`
##### 3.4: Now that the venv was created, we can activate it by running `venvname\scripts\activate.bat`. The name of the venv should be displayed in from of every command from now on
##### 3.5: The activated venv makes it so every change made is local to this project, and does not affect the rest of our system

#### Step4: Interpreter
The Interpreter controls what version of python to use when running code. Since we are using a venv, the interpreter should be set to python venv, and not your default installation of python
To check which interpreter you are using navigate to the bottom right of the window where the numerical version of python is displayed
If you are using the correct version the word "venv" should be next to the version
If not click on it and choose the correct version

#### Step5: Installing libraries
Now that the venv is activated, we can intall libraries with `pip install libraryname`
We can also delete them, or show information about them with `pip uninstall` and `pip show` respectively

#### Step6: Requirements
To keep track of library versions, and to make it easier for someone else to run the code, we create a "requirements.txt" file
In this file, we add the libraries we have installed and their respective version in this format `libraryname==1.2.3`
To find the full name of the library and the version we are using, we run `pip show libraryname` in cmd
Everytime we make a change to the libraries of the project, we will also alter this file accordingly

# Basic guide on how to upload on github

#### Step1: Download git
Open a new cmd (not the one with the activated venv)
Check if git is installed in your system by running `git --version`
If not installed, download from the official website

#### Step2: Create repository
Create a new repository on github
After creating, you will be given a link to the repository similar to `"https://github.com/username/repositoryname.git"`

#### Step3: git and commit locally
##### 3.1: We can create a ".gitignore" plain text file and add everything that we dont want to upload, for example the "venv/" subdirectory
##### 3.2: Initiate git by running `git init`
##### 3.3: Prepare all files for upload by running `git add .`
##### 3.4 Every directory inside the ".gitignore" file will be excluded automatically
##### 3.5: Check what is prepared by running `git status`
##### 3.6: Set your name and email by running `git config user.name "yourname"` and `git config user.email "youremail"` respetively
##### 3.7: Commit the files by running `git commit -m "message here"`
##### 3.8: To inspect all previous commitments we can run `git log`, which will also show the commit hash code 

#### Step4: git and commit remotely
##### 4.1: Add the github repository as a remote repository by running `git remote add origin` followed by the repository url you where provided earlier `git remote add origin https://github.com/username/repositoryname.git`
##### 4.2 To get the list of all remote repositories run `git remote -v`
##### 4.3: To push commitments to remote repository run `git push origin branchname`. you can find the branch name with  `git status`
