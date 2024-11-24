# Creating Python Virtual Environment in Windows and Linux

Last Updated : 22 Aug, 2023

A Virtual Environment is a Python environment, that is an isolated working copy of Python that allows you to work on a specific project without affecting other projects So basically it is a tool that enables multiple side-by-side installations of [Python](https://www.geeksforgeeks.org/python-programming-language/), one for each project.

#### **Creating a Python virtual environment in Linux**

If pip is not in your system

```
$ sudo apt-get install python-pip

```

Then install virtualenv

```
$ pip install virtualenv

```

Now check your installation

```
$ virtualenv --version

```

Create a virtual environment now,

```
$ virtualenv virtualenv_name

```

After this command, a folder named

**virtualenv\_name**

will be created. You can name anything to it. If you want to create a virtualenv for specific python version, type

```
$ virtualenv -p /usr/bin/python3 virtualenv_name

```

or

```
$ virtualenv -p /usr/bin/python2.7 virtualenv_name

```

Now at last we just need to activate it, using command

```
$ source virtualenv_name/bin/activate

```

Now you are in a Python virtual environment You can deactivate using

```
$ deactivate

```

#### **Creating Python virtualenv in Windows**

If python is installed in your system, then pip comes in handy. So simple steps are: 1) Install virtualenv using

```
 > pip install virtualenv 

```

2\)Now in which ever directory you are, this line below will create a virtualenv there

```
 > python -m venv myenv

```

And here also you can name it anything. 3) Now if you are same directory then type,

```
 > myenv\Scripts\activate

```

You can explicitly specify your path too. Similarly like Linux you can deactivate it like

```
$ deactivate

```

\
