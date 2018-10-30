# Lesson 1: Python Intro Review

Now that you have Python 3.6.4 downloaded and your favourite IDE installed, 
let's review the topics that we touched on in our _HelloWorld_ lesson.

###Statements

First we executed a program with a single line in it:
```python
print("Hello World")
```
We got `Hello World` in our console. We can call this single line of 
code a _statement_. A Python program is made up of several statements.

###Inputs and Outputs | Variable Assignment | String Concatenation
This `print` _statement_ is called **output** and is one way of interacting 
with the user. There are several different ways to produce output, 
eg.creating and writing to a file.

Another way of interacting with the user is through **input**.
We wrote a few lines of code that:
1. Took input from the user using the `input` function
2. Used **variable assignment** to store the the input in the variable 
`name` 
3. Printed out a specialised greeting using **string concatenation** 
with the **+** operator:
```python
name = input("What's your name? ")
print("Hello "+ name)
```

Our output looked like this:
> What's your name? _Liz_
>
>Hello Liz

###Getting Help
While typing the function name `input` you may have noticed this popup:

![alt text][input_suggestion]

This is one of the many benefits that come with using an IDE - autocomplete with suggestions!

Sometimes this short definition won't be enough and we may need more information. 
We can find out more about a function or statement by using the built-in `help` functionality. 

The following is output from typing `help(input)` into the Python console.

![alt text][help_command]

###Tips
> Shift + F10 will run code in PyCharm!

> Ctrl + / will comment out the selected line of code
```python
# This is a comment
```

[input_suggestion]: ../resources/input_suggestion.PNG "IDE autocomplete suggestion"
[help_command]: ../resources/help_example.PNG "Python `help` command"
