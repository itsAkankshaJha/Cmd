## Cmd commands 

### 1.  To move to a certain directory 
        cd [name of directory] // donot place these brackets 
 Example : <br>
    **C:\Users\DELL> cd Desktop** , We will land in desktop folder . <br>
   **C:\Users\DELL\Desktop> cd virtualenv** , Here we will land in virtualenv which is inside Desktop . <br>
### 2 . To change directory or path 
         cd /D [folder path ]
         
         
 ![cmd](https://user-images.githubusercontent.com/72215893/124272539-816fe400-db5c-11eb-954d-d0b0a5d892d7.png)
 
 Look , The directory path has changed.
 
### Virtual environment
A virtual environment is a tool that helps to keep dependencies required by different projects separate by creating isolated python virtual environments for them.  

__Why virtual environment?__  
Imagine a scenario where you are working on two web based python projects and one of them uses a Django 1.9 and the other uses Django 1.10 and so on. In such situations virtual environment can be really useful to maintain dependencies of both the projects  
__Where to use virtual environment?__  
By default, every project on your system will use these same directories to store and retrieve site packages (third party libraries).  
Python since it can’t differentiate between versions in the “site-packages” directory. So both v1.9 and v1.10 would reside in the same directory with the same name. To solve this problem, we just need to create two separate virtual environments for both the projects.  
To solve this problem, we just need to create two separate virtual environments for both the projects.  
We use a module named virtualenv which is a tool to create isolated Python environments. virtualenv creates a folder which contains all the necessary executables to use the packages that a Python project would need.

#### commands to install virtual environment:

- __To install virtual environments__
      
       pip install virtualenv

- - __to check the version:__  <br>
        
        virtualenv -- version

- __to create a virtual environment:__ <br>
              
           virtualenv name    
After running this command, a directory named my_name will be created. This is the directory which contains all the necessary executables to use the packages that a Python project would need.
- If you want to specify Python interpreter of your choice, for example Python 3, it can be done using the following command:<br>

              virtualenv -p /usr/bin/python3 virtualenv_name  
- __To create a Python 2.7 virtual environment, use the following command:__  

       $ virtualenv -p /usr/bin/python2.7 virtualenv_name  

- __After creating virtual environment, you need to activate it. Remember to activate the relevant virtual environment every time you work on the project.
Command for activation:__ <br>

          source virtualenv_name/bin/activate
          
**If this doesn't work then we can use this command (where our scripts folder is located)**<br>
            
          C:\> virtualenv\Scripts\activate
          
- Now you can install dependencies related to the project in this virtual environment.

- __Once you are done with the work, you can deactivate the virtual environment by the following command:__

      (virtualenv_name)$ deactivate
  
  


### steps with python 3:(3.8)
- have python installed
- have pip installed
- pip install virtualenv
- cd (the folder where virtual env has to be created)
- virtualenv _name of the virtual env to be given_ . Ex : virtaulenc venv    (a folder name venv will be created in the location, containing a set of files likw scripts etc)
- venv\Scripts\activate ( then it looks like: (venv) C:\Users\PRAGY\Desktop\rasa project>  (depending on your addresses)) . The virtual env is now active. (Note: venv is the name of our virtual env)
- to install packages/ dependencies, . For example if you are using Django 1.9 for a project, you can install it like you install other packages. command :(virtualenv_name)$ pip install Django==1.9. The Django 1.9 package will be placed in virtualenv_name folder and will be isolated from the complete system.  
- (virtualenv_name)$ deactivate : command to deactivate the virtual env , once the work is done.

Python virtual env documentation link: https://docs.python.org/3/library/venv.html   
https://docs.python.org/3/tutorial/venv.html (commands to be used inside virtual env)

--------------------------------------------

### Difference between venv and virtualenv:
venv is a subset of virtualenv integrated into the standard library since Python 3.3. The subset meaning that only part of virtualenvs functionality is in venv:

➡️venv can be slower since it does not have "app-data seed method"  
➡️venv is only upgraded via upgrading the Python version, while virtualenv is updated using pip.  
➡️venv is not extendable  
:arrow_right: virtualenv have more rich programmatic API (describe virtual environments without creating them). See the venv API here.  
➡️venv cannot automatically discover arbitrarily installed python versions, while virtualenv does. This means, that with venv you have to specify the full path of the python executable, if you want to use some other python version than the first one in the PATH. With virtualenv, you can just give the version number. See python discovery in the virtualenv documentation.  
To me the differences are quite subtle and the only practical difference has been that **venv is included in the standard library (since 3.3)**. I have been using python -m venv venv for a long time and have never needed an alternative.

source: stack overflow

--------------------------------------------------------------
