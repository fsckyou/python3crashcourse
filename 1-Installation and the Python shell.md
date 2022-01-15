# 1. Installation and the Python shell

## Summary
This section describes how to install Python3 and how to access the Python shell from the command line. 

## Installation
### Windows
Using the Microsoft Store, search for Python 3 and install the latest release
### Mac
Go download the official installer from the [Python download website](https://www.python.org/downloads/)
### Linux
Check what's installed first
```sh
$ python3 --version 
```
If you get a version number, then you're good. Otherwise, follow a guide like this [one](https://docs.python-guide.org/starting/install3/linux/) 

You should also install a few more packages to have a good setup
```sh
$ sudo apt install -y build-essential libssl-dev libffi-dev python3-dev python3-pip
```

##  The Python shell
Python offers an interactive shell where you can run commands line by line and get results in realtime. Run this command to access the Python shell. The Python shell is also called a REPL. REPL stands for **R**ead-**E**xecute-**P**rint-**R**epeat because that's exactly what it does.
```sh
$ python3
```
You should see something like this now....
```
Python 3.9.7 (tags/v3.9.7:1016ef3, Aug 30 2021, 20:19:38) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
In this shell, you can enter anything that would be a valid line of Python. For now, let's just use it like a calculator.
```py
>>> 3 * 9
27
>>> 
```
Mathematical operators to try out in Python

| Operator    |   Name         |  Example   |
| ----------- | -------------- | ---------- |
|     +       | Addition       |   2 + 2    |
|     –	      | Subtraction    |   3 – 1    |
|     *       | Multiplication |   5 * 3    |
|     /       | Division       |   5 / 2    |
|     %       | Modulus        |   5 % 2    |
|     //      | Floor Division |   5 // 2   |
|     **      | Exponential    |   5 ** 2   |

You can also use parentheses to control precedence
```py
>>> (2 + 3) * 3
15
```
Tip: You can use _ to get the previous result.
```py
>>> 3 * 3
9
>>> _ + 3
12
```
[2. Variables](<2-Variables.md>)
