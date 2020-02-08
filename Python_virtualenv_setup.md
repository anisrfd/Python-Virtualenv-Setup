# Python-Virtual-env-Setup


How to set up a Python development environment :
==============================================
For setup virtual environment you must need python environment in your OS system.

A Python development environment is a folder which you keep your code in, plus a "virtual environment" which lets you install 
additional library dependencies for that project without those polluting the rest of your desktop/laptop.

    mkdir my-newproject
    cd my-newproject 
    virtualenv --python=python3.7 venv
    # This will create a my-new-python-project/venv folder
    touch .gitignore
    subl .gitignore
    # Add venv to your .gitignore

Now any time you want to work on your project, you need to "activate your virtual environment". Do that like this:

    cd my-newproject
    source venv/bin/activate

You can tell it is activated because your terminal prompt will now look like this:

    (venv) computer:my-newproject user$ 

Note the (venv) bit at the start.

If you get an error like : 

"source : The term 'source' is not recognized as the name of a cmdlet, function, script file, or operable program.
Check the spelling of the name, or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ source venv/bin/activate
+ ~~~~~~
    + CategoryInfo          : ObjectNotFound: (source:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException"  

then try this:
   #To install :
    
     pip install --user virtualenv 
   
   #To create a virtual environment (venv):
     
     python -m virtualenv venv
    
   #To activate:
     
     -cd venv
     
     -cd Scripts
      
     -activate.bat
   #If get error on VS code shell "source couldn't recognize" then try this: 
      
      - open the folder with any gitbash console. for example using visualCode and Gitbash console program: 
      1)Install Gitbash for  windows 
      2) using VisualCode IDE, right click over the project open in terminal console option
      3) on window console in Visualcode, looking for a Select->default shell and change it for Gitbash
      4)now your project is open with bash console and right path, put source ./Scripts/activate
      btw : . with blank space = source
   
   #if you get an error on activate.bat then try 
     
     .\activate.bat or activate
    
   #to deactivate:
     
     -deactivate.bat or deactivate
    
   #to run venv again just type
   
     -activate.bat or .\activate or activate


Once it is activated, any time you run the "python" or "pip" commands it will be running the special custom versions in your venv folder.

You could also run them without activating the virtual environment like this:

    venv/bin/python
    venv/bin/pip

To install new python libraries, use pip like this:

    pip install requests
    pip install ipython

It's always a good idea to install ipython.
