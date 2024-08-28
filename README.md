Below is a basic guide to how to initiate a python project in vscode

Step1: Folder
We create a folder for the project, then open said folder in vscode

Step2: Files
We create a new python file (.py) inside the folder using vscode with File>New File...

Step3: Venv
We want to create a venv for this project. A venv allows for installation of libraries inside the project, not affecting the system as a whole
3.1: Open a cmd terminal in vscode by navigating the the terminal panel (located at the bottom of the window) and clicking on the arrow next to the (+) sign, then selecting cmd
3.2: Locate the installation of python in your system by running (where python), for example "C:\Users\User\AppData\Local\Python\Python312\python.exe"
3.3: Now copy and paste the installation, then type "-m venv", and a name for the venv (for example venv)
3.4: It should look like this "C:\Users\User\AppData\Local\Python\Python312\python.exe -m venv venvname". Run the command to create the venv
3.5: Now that the venv was created, we can activate it by running "venvname\activate\scripts.bat". The name of the venv should be displayed in from of every command from now on
3.6: The activated venv makes it so every change made is local to this project, and does not affect the rest of our system

Step4: Interpreter
The Interpreter controls what version of python to use when running code. Since we are using a venv, the interpreter should be set to python venv, and not your default installation of python
To check which interpreter you are using navigate to the bottom right of the window where the numerical version of python is displayed
If you are using the correct version the word "venv" should be next to the version
If not click on it and choose the correct version

Step4: Installing libraries
Now that the venv is activated, we can intall libraries with "pip install libraryname"
We can also delete them, or show information about them with "uninstall" and "show" respectively

Step5: Requirements
To keep track of library versions, and to make it easier for someone else to run the code, we create a "requirements.txt" file
In this file, we add the libraries we have installed and their respective version in this format "libraryname==1.2.3"
To find the full name of the library and the version we are using, we run "pip show libraryname" in cmd
Everytime we make a change to the libraries of the project, we will also alter this file accordingly
