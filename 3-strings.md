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
Oh yeah - subtraction and other arithmetic operations aren't possible.

## Quotes
Should you use `'` or `"` to encapsulate strings? 
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
