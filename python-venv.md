## How Can You Work With a Python Virtual Environment?

Creating a Python virtual environment allows you to manage dependencies separately for different projects, preventing conflicts and maintaining cleaner setups. With Python's venv module, you can create isolated environments that use different versions of libraries or Python itself.


### Create It

Windows,Linux, macOS:

```sh
python -m venv .venv
```

This command creates a new virtual environment named .venv using Python's built-in venv module. The first venv that you use in the command specifies the module, and the second .venv sets the name for your virtual environment. You could name it differently, but calling it .venv is a good practice for consistency.


### Activate It

Windows:

```sh
.venv\Scripts\activate
```

Linux, macOS:

```sh
source .venv/bin/activate
```

Before you run this command, make sure that you're in the folder containing the virtual environment you just created.

If youve named your virtual environment something other than .venv, then you'll have to use that name in the path instead of venv when you source the activation script.

### Install Packages Into It

After you've created and activated your virtual environment, you can install any external dependencies that you need for your project.

Windows, Linux, macOS:

```sh
python -m pip install <package-name>
```

> Note: Since you created your virtual environment using a version of Python 3, you don't need to call python3 or pip3 explicitly. As long as your virtual environment is active, python and pip link to the same executable files that python3 and pip3 do.


### Deactivate It

Once you're done working with this virtual environment, you can deactivate it.

```sh
deactivate
```

## How to Save and Restore Python Dependencies

If you're working on one computer and want to move your Python project to another system (or share it with someone else), you can use ```pip freeze``` to save your dependencies and later restore them.

Step 1: Save dependencies to a text file

```sh
python -m pip freeze > requirements.txt
```

```
numpy==1.24.2
pandas==2.1.0
requests==2.31.0
```

#### Want to just see installed packages?

```sh
pip freeze
```
or 

```sh
pip list
```

Step 2: Transfer and restore dependencies on another system

Create a new virtual environment:
```sh
python -m venv .venv
```
Activate the virtual environment:
```sh
source .venv/bin/activate  # On Linux/Mac
.venv\Scripts\activate    # On Windows

```
Make sure requirements.txt is in the project folder, then run:
```sh
pip install -r requirements.txt
```

This installs all the packages with the exact versions you had before.


## Why this is useful

* Keeps your project consistent across different systems.
* Ensures compatibility and avoids version conflicts.
* Essential for teamwork, deployment, and long-term maintenance.

