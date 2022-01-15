# 7. First Program

## Summary

Entering the code in the REPL
Let me share the program first.
```py
def say_hi(name):
    if name == '':
        print("You didn't enter your name!")
    else:
        print("Hi there...")
        for letter in name:
            print(letter)
name = input("Your name: ")
say_hi(name)
```
When typing in more than a few lines of code, you have to be very careful with indentation. If you keep getting errors because of formatting or indentation, you can also try to completely copy and paste the code. In the REPL, it should end up looking like the following:
```py
>>> def say_hi(name):
...     if name == '':
...         print("You didn't enter your name!")
...     else:
...         print("Hi there...")
...         for letter in name:
...             print(letter)
... 
>>> name = input("Your name: ")
 < enter your name at this point >
>>> say_hi(name)
```

## Interactive analysis time!
Let's go through what's happening as a class

## How about this?
Create an infinite loop that keeps asking for names,
and that keeps greeting us using the entered name.

---
[Prev: Functions](<6-Functions.md>)   |   [Next: Comments](<8-Comments.md>)