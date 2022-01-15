# 4. Booleans

## Summary
Booleans are yet another datatype. They are either `True` or `False` and never anything else. That's it!
## Simple, yes, but used ALL the time
In computer science, booleans are used a lot. This has to do with how computers work internally. Many operations inside a computer come down to a simple “true or false.”

In Python, we use booleans in combination with conditional statements to control the flow of a program:
```python
>>> door_is_locked = True
>>> if door_is_locked:
...     print("Mum, open the door!")
...
Mum, open the door!
```
First, we define a variable called door_is_locked and set it to True. Next, you’ll find an if-statement. This is a so-called conditional statement. It is followed by an expression that can evaluate to either `True` or False. If the expression evaluates to True, the block of code that follows is executed. If it evaluates to `False`, it is skipped. Go ahead and change door_is_locked to `False` to see what happens.

An if can be followed by an optional else:
```python
>>> door_is_locked = False
>>> if door_is_locked:
...     print("Mum, open the door!")
... else:
...     print("Let's go inside")
...
Let's go inside
```
Thanks to our else-block, we can now print an alternative text if door_is_locked is False.
## Python’s Boolean Operators
The ability to use conditions is what makes computers tick; they make your software smart and allow it to change its behavior based on external input. We’ve used `True` and `False` directly so far, but more expressions evaluate to either `True` or `False`. These expressions often include a so-called boolean operator.

Let’s look at these boolean operators in the REPL:
```python
>>> 2 > 1
True
>>> 2 < 1
False
>>> 2 < 3 < 4 < 5 < 6
True
>>> 2 < 3 > 2
True
>>> 3 <= 3
True
>>> 3 >= 2
True
>>> 2 == 2
True
>>> 4 != 5
True
>>> 'a' == 'a'
True
>>> 'a' > 'b'
False
```
This is what all the boolean operators are called:

| Operator  |   Meaning                     |
|-----------|-------------------------------|
| >         |   greater than                |
| <         |   smaller than                |
| >=        |   greater than or equal to    |
| <=        |   smaller than or equal to    |
| ==        |   is equal                    |
| !=        |   is not equal                |
## Python’s boolean operators
As can be seen in the examples, these operators work on strings too. Strings are compared in the order of the alphabet, with these added rules:
- Uppercase letters are ‘smaller’ than lowercase letters, e.g.: ‘M’ < ‘m’
- Digits are smaller than letters: ‘1’ < ‘a’

You’re probably wondering what the logic is behind these rules. Internally, each character has a number in a table. The position in this table determines the order. It’s as simple as that. See Unicode on Wikipedia to learn more about it if you’re interested.