# Motivation
Before you run, you must learn to walk. In programming, learning to walk requires a thorough understanding of the fundamentals. Upon mastering the fundamentals, we will be able to advance our skills very quickly. So, be excited and meticulous in your work in these initial exercises. These are truly the foundation of complex and high level abstract programming. By the time we are done, we will be constructing machine learning graphics applications.

# Basic Terminal Commands
Let's take a moment to both recall the three main command line programs we have been using and recap how exactly command line programs work.

## Some nifty command line tools
* ls - list contents of current directory
* cd - change directory 
* vim <filename> - open a file in vim

## How do command line programs work?
All command line programs follow this simple calling convention: the name of the program, followed by any options specific to that program.

Let's look at this command, for example:
```
cd code
```
This command would execute the program `cd` (change directory). `cd` itself takes one mandatory option: you must specify which directory you would like to change _to_. So, in this case, `code` is the directory we would like to change to. `cd` is the program. `code` is the option specific to `cd`.


Now, this command:
```
vim some_file.py
```
If `some_file.py` already exists, this will open the program `vim` to edit it. If it doesn't, it will create a new file called `some_file.py` and open it for editing. 


# If Statements
If statements are a type of _control flow_ statement. _Control flow_ here, despite initial impressions, does not have anything to do with bladder health. If statements are one way in which you can control the flow of your program.

Up until this point, there has been one sacred fact that has been with you since you started working with Python: code is executed line-by-line, top-to-bottom. That is how the program _flows_, top-to-bottom, line-by-line.

Consider the following example:
```python
print("hi")
print("this is")
print("python")
```

The output of this program will be:
```
hi
this is
python
```

Before moving on to mastering if statements, make sure that this default flow of top-to-bottom makes sense. Code is, by default, executed in order and without fuss. If statements are where those defaults can be changed, and we can opt out of executing certain sections of code. An if statement looks like this:
```python
if (bool):
  do_something()
```

This can be read as:
> If _bool_ is true, then `do_something`

Note the formatting -- it is important. An if statement is followed by a colon, and then an indented section of code. That indented section of code is what is conditionally executed. Conditionally executed meaning it either is executed, or it isn't, based on some condition. That condition is the `bool` inside of the parenthesis after the word `if`. You can do many things in an if statement, and exiting the indentation exits the if statement:
```python
if (bool):
  do_something()
  do_something_else()
  print("Still in the if statement!")
print("now I'm outside of the if statement")
```
## Real examples of if statements
You already have an example from our last class:
```python
x = len(input())
if (x < 5):
  print("I know that word!")
else:
  print("I don't know any words that long.")
```

This example uses an `else`. Let's ignore that for now, and we will come back to that next time.

The following is another example of an if statement which will say "hi" if the user says "hello", and "bye" if the user says "goodbye".
```python
user_input = input()
if (user_input == "goodbye"):
  print("bye")
if (user_input == "hello"):
  print("hi")
```

# Exercises
These exercises have been designed to practice only the skills we have learned thus far. They may feel repetitive. We are essentially doing programming "reps", just like you would do reps of curls in the gym. The idea is to get comfortable writing files from scratch and performing these operations without instructor prompting.

To submit an exercise, attach the .py file to an email and send it to my email (which I have sent to you separately). I will provide feedback promptly. Should you get stuck, contact me and I will give you just enough hints to keep moving.

## Exercise 1
1. What command allows you to move around in the terminal by changing directories?
2. What command lists the contents of your current directory in the terminal?
3. How do you open a file in vim?
4. How do you save and exit vim?
5. How do you run a python file in the command line? (hint: `python3`)

## Exercise 2
Write a Python program which gets user input and prints out the length (`len`) of that input.

Sample input:
```
hello
```
Sample output:
```
5
```
## Exercise 3
Write a Python program which gets user input and, if the user input is the string "heavy", prints out "metal". Otherwise, do nothing.

Sample input 1:
```
heavy
```

Sample output 1:
```
metal
```

Sample input 2:
```
light
```
Sample output 2:
```

```

## Exercise 4
Write a Python program which gets user input and casts it to a number (`int`). Print out that number multiplied by two.

Sample input:
```
10
```
Sample output:
```
20
```
## Exercise 5
Write a Python program which gets user input and casts it to a number. If that number is a multiple of five, print out "this number is a multiple of five". Otherwise, print out "this number is not a multiple of five".

Sample input 1:
```
15
```

Sample output 1:
```
this number is a multiple of five
```

Sample input 2:
```
12
```
Sample output 2:
```
this number is not a multiple of five
```
