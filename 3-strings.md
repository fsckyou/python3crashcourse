# 3. Strings

## Summary
It's text time! A string is a datatype that holds characters and text.
```python
>>> "Hello, World!"
'Hello, World!'
```
Quotes tell Python that the text inside is a string.

## Operations with Strings
Weirdly, you can do things like add and multiply strings. Here's how that works:
```python
>>> 'a'+'b'
'ab'
>>> 'ab' * 4
'abababab'
>>> 'a' - 'b'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for -: 'str' and 'str'
```
Oh yeah; subtraction and other arithmetic operations aren't possible, but there are other ways to manipulate strings, as you'll see later.

## Quotation marks
Should you use `'` or `"` to encapsulate strings? Turns out you can use either!
```python
>>> "This is good"
'This is good'
>>> 'This is ok'
'This is ok'
>>> 'How's this?'
  File "<stdin>", line 1
    'How's this?'
         ^
SyntaxError: invalid syntax
>>> 'How\'s this?'
"How's this?"
>>> "And this's ok"
"And this's ok"
```
As you can see, using an apostrophe inside a single quoted string can be problematic, but you can overcome this by **escaping** the apostrophe. Similarly, if you want to put a quotation mark inside a string that's encapsulated in `"`s you must escape that. 

One more thing... let's say you've got a long string that you want to store with multiple lines... Try this:
```python
>>> a_big_string = """This is the first line,
... this is the second line,
... and this is a third."""
```
As a bonus, you can use triple quotation marks if you want to not need to worry about escaping `'` and `"` characters.
```python
>>> silly_string = """There's a good quote I heard once: "Hello, World!" Ok, it's not that great."""
```
## String manipulation!
Alright, so you have that shiny new string and you want to do something with it? Well Python comes with a whole bunch of functions that you can use to modify them.
```python
>>> mystring = "test string"
>>> mystring.
mystring.capitalize(    mystring.find(          mystring.isdecimal(     mystring.istitle(       mystring.partition(     mystring.rstrip(        mystring.translate(
mystring.casefold(      mystring.format(        mystring.isdigit(       mystring.isupper(       mystring.replace(       mystring.split(         mystring.upper(
mystring.center(        mystring.format_map(    mystring.isidentifier(  mystring.join(          mystring.rfind(         mystring.splitlines(    mystring.zfill(
mystring.count(         mystring.index(         mystring.islower(       mystring.ljust(         mystring.rindex(        mystring.startswith(
mystring.encode(        mystring.isalnum(       mystring.isnumeric(     mystring.lower(         mystring.rjust(         mystring.strip(
mystring.endswith(      mystring.isalpha(       mystring.isprintable(   mystring.lstrip(        mystring.rpartition(    mystring.swapcase(
mystring.expandtabs(    mystring.isascii(       mystring.isspace(       mystring.maketrans(     mystring.rsplit(        mystring.title(
```
Check out the official Python [documentation](https://docs.python.org/3/library/stdtypes.html#textseq) to learn what each of these functions does and how to use them. Feel free to play with one or more of these now.

## Getting the string length
A common operation is to get the string length. Unlike the operations above, this can be done with Python’s len() function like this:
```python
>>> len("I wonder how long this string will be...")
40
>>> len(mystring)
11
```
In fact, the len() function can be used on many objects in Python, as you’ll learn later on. If functions are new to you, you’re in luck, because our next page will explain exactly what a function in Python is, and how you can create one yourself.

## Split a string
Another common operation is splitting a string. For this, we can use one of the built-in operations, conveniently called split. Let’s start simple, by splitting up two words on the space character between them:
```python
'Hello world'.split(' ')
['Hello', 'world']
```
The split operation takes one argument, which is the sequence of characters to split on. The output is a Python list, containing all the separate words.

## Split on whitespace
A common use-case is to split on whitespace. The problem is that whitespace can be a lot of things. Three common ones that you probably know already are:

- space characters
- tabs
- newlines

But there are many more, and to make it even more complicated, whitespace doesn’t mean just one of these characters, but can also be a whole sequence of them. E.g., three consecutive spaces and a tab character form one piece of whitespace.

Exactly because this is such a common operation among programmers, and because it’s hard to do it perfectly, Python has a convenient shortcut for it. Calling the split operation without any arguments splits a string on whitespace, as can be seen below:
```python
>>> 'Hello \t\n there,\t\t\t stranger.'.split()
['Hello', 'there,', 'stranger.']
```
As you can see, no matter what whitespace character and how many, Python is still able to split this string for us into separate words.

## Replace parts of a string
Let’s look at one more built-in operation on strings: the replace function. It’s used to replace one or more characters or sequences of characters:
```python
>>> 'Hello world'.replace('H', 'h')
'hello world'
>>> 'Hello world'.replace('l', '_')
'He__o wor_d
>>> 'Hello world'.replace('world', 'readers')
'Hello readers'
```
## Reversing a string
A common assignment is to reverse a Python string. There’s no reverse operation, though, as you might have noticed when studying the list of operations like `lower()` and `upper()` that comes with a string. This is not exactly beginner stuff, so feel free to skip this for now if you’re going through the tutorial sequentially.

To reverse a string efficiently, we can treat a string as a list. Lists are covered later on in this tutorial. In fact, you could see a string as a list of characters. And, more importantly, you can treat it as such. List index operations like `mystring[2]` work just like they work on lists:
```python
>>> mystring = 'Hello world'
>>> mystring[2]
'l'
>>> mystring[0]
'H'
```
Note that in Python, like in all computer languages, we start counting from 0.

What also works exactly the same as in lists, is the slicing operator. Details of list slicing can be found on the Python list page and won’t be repeated here. If you’re coming from other languages, you might compare it to an operation like substring() in Java, which allows you to retrieve specific parts of a string.

Slicing in Python works with the slicing operator, which looks like this: mystring[start:stop:step_size]. The key feature we use from slicing is the step size. By giving the slicing operator a negative step size of -1, we traverse the string from end to beginning. By leaving the start and end position empty, Python assumes with want to slice the entire string.

So we can use slicing to reverse a Python string as follows:
```python
>>> mystring = 'Hello world'
>>> mystring[::-1]
'dlrow olleH'
```
## Python string format with f-strings
A common pattern is the need to merge some text strings together or use a variable inside your string. There are several ways to do so, but the most modern way is to use f-strings, short for formatted strings.

Let’s first look at an example, before we dive into the details:
```python
>>> my_age = 40
>>> print(f'My age is {my_age}')
My age is 40
```
The f-string looks like a regular string with the addition of an f prefix. This f tells Python to scan the string for curly braces. Inside these curly braces, we can put any Python expression we want. In the above case, we just included the variable my_age. F-strings provide an elegant way of including the results of expressions inside strings.

Here are a couple more examples you can try for yourself as well, inside the REPL:
```python
>>> f'3 + 4 = {3+4}'
'3 + 4 = 7'
>>> my_age = 40
>>> f'My age is, unfortunately, not {my_age-8}'
'My age is, unfortunately, not 32'
```

---
[Prev: Variables](<2-Variables.md>)   |   [Next: Booleans](<4-Booleans.md>)