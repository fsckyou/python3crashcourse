# 2. Variables

## Summary
Ok so now you can do simple calculations in Python, but what if you want to store and recall information? Well....

## What is a Variable?
A variable is used to store information that can be referenced later

## Declaring a Python Variable
Try this:
```python
>>> result
```
What happens?

What you see is how Python shows you an error. The error in this case is that the variable "result" hasn't been declared. You _declare_ a variable by assigning a value to a name. Like this:
```python
>>> result = 3 * 5
>>> result
15
>>> result - result/2
7.5
>>> 
```
### Variable Naming Rules
Can I name a variable `Steve`? `fr3d`? `123`? `1var`? `_hi_`? Some work and some don't. There are some rules for what makes a valid variable name.

Valid variable names can only contain:
* Lowercase and uppercase letters: a-z and A-Z
* Numbers: 0-9
* Underscores: _

Additionally, there are these two rules:
* Variable names must start with a letter or the underscore character, and can not start with a number.
* Names are case-sensitive

### Good Practices for Variable Naming
Make your variable names as descriptive of what you're storing as possible. You'll thank yourself later when picking up an old project. It also helps other people to more easily read and understand your code. Python variable name convention is to use all lowercase with underscores (_) separating word. For example: `shopping_cart_total`.

### Datatypes
So far we've been working with numbers. Numbers come in a few flavors in Python: **int** which is short for integer, and **float** are the two most common. An **int** holds whole numbers like `-4, 15, and 42069`. A **float** holds decimals like `4.0, 7.205, and 69.420`. Unlike other programming languages, we don't have to explicitly tell Python variable types. It's smart enough to ensure that variables will always hold whatever is assigned to them. 

If you ever want to know what datatype a variable is holding, use something called the "type" function. 
```python
>>> sum_total = 1 + 2 + 1.5
>>> sum_total
3.5
>>> type(sum_total)
<class 'float'>
```
Next we'll learn all about another datatype for text!

---
[Prev: Installation and the Python Shell](<1-Installation and the Python shell.md>)   |   [Next: Strings](<3-Strings.md>)