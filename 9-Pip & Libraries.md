# 9. Pip & Packages & Projects

## Summary
Packages are what make Python such a popular language. They generally will make life easier!

## Packages
A package is a bunch of code that is grouped together to perform a function or set of functions.
 
## What's out there?
SO MUCH!! Go have a look on [PyPi](https://pypi.org) The Python Package Index.

## How do I get what I want?
Let's say you've gone and explored and you found that you really want the [pyramid-text](https://pypi.org/project/pyramid-text/) package for generating pyramid text. I mean, I won't judge you...

There are two steps to getting and using this package. 
1. Use pip3 (the 3 for Python 3) to download the package. From your command line (NOT the Python shell):
```
$ pip3 install pyramid-text

(then you'll see something like this)

Collecting pyramid-text
  Downloading pyramid-text-1.0.tar.gz (1.1 kB)
Installing collected packages: pyramid-text
    Running setup.py install for pyramid-text ... done
Successfully installed pyramid-text-1.0
```
2. Import it into your program so you can use it. How to use your specific package can be found on that package's homepage or in its documentation - that can vary. For pyramid-text, however, the documentation is here: [https://github.com/infernyan/pyramid-text](https://github.com/infernyan/pyramid-text)
```py
import pyramidtext

print(pyramidtext.generate("Hello World!"))
```
This same process works for any package you can find!