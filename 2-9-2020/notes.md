# Notes from 2/9/2020
## Vim Tips
1. There are two main modes in Vim. "Normal" mode, for entering commands, and "insert" mode, for typing text. In insert mode, hit `Esc` to return to normal mode. 
2. Use `:<number>` in normal mode to navigate to a line number. e.g., `:19` would take you to line 19. 
3. Use `/` in normal mode to search for things. e.g. `/python` would search the current file for the text "python".
4. Use `o` in normal mode to make a new line below the current line and enter insert mode.
5. Use `i` in normal mode to enter insert mode before the cursor position. `I` enters insert mode at the beginning of the line.
6. Similar to the above, `a` in normal mode enters insert mode after the cursor position. `A` enters insert mode at the end of the line.

## Python Stuff
### Variables
Consider the following code.
```python
x = 5
y = 10
```
In this example, `x` and `y` are _variables_. A variable is a method of storing values. Here, `x` has stored the value `5`, and `y` has stored the value `10`. A variable's name must:
- contain no whitespace (spaces, tabs, or newlines)
- begin with a letter or underscore
- contain only letters, numbers, or _ (note that it cannot start with a number)
- are case sensitive
- not be a word used by the language for other reasons

Some example valid variable names are:
- `x`
- `y`
- `_variable`
- `__python_is_cool`
- `PYTHON_yay`
- `variable_1`
- `Variable_1`
 
Note that `variable_1` and `Variable_1` would be different variables, as variable names are case sensitive.

Some _invalid_ variable names are:
- `2x` (starts with a number)
- `for` (this keyword is reserved for other uses)
- `a variable` (this name contains whitespace)

#### Variables Exercise
Open up your REPL and declare some variables. 
- Can you change a variable's value by re-assigning it to something else? 
- Can you add one variable to another? 
- What happens if you add two string variables together? i.e., what happens when you execute the following code?
```python
x = "python"
y = "is cool"
x + y # What happens here?
```

### Types
Every value has a _type_. To see the type of a value, run `type(value)` in your REPL. For example,
- `type(5)` is `<class 'int'>`, meaning it is an integer.
- `type("foo")` is `<class 'str'>`, meaning it is a string.
- `type(True)` is `<class 'bool'>`, meaning it is a boolean.


- An integer is a whole number. e.g. `1`, `2`, `123401293447`
- A float is a number with a decimal point e.g. `5.2` or even `5.0`.
- A string is text enclosed in quotes. e.g. `"foo"`, `"100"`, or even an empty string `""`
- A boolean is a true or false value (named for [George Boole](https://en.wikipedia.org/wiki/George_Boole)). There are only two examples: `True` and  `False`.

### Getting User Input In Python
Oftentimes, when writing a program, you, as the programmer, would like to interact with the user (who often is also you `:)` ). To get input from the user in your program, Python includes a function called `input()`. Consider the following code snippet.
```python
userInput = input()
print(type(userInput))
print("you typed: ", userInput)
```
If you run this code, you will see that it prints back whatever you typed in, as well as `<class 'str'>`, from the second line. The type of user input is always a string (text). If you want it to be a different type, you must convert it into that type. If it is not convertable, like you try to convert `yolo` into an integer, the program will crash.

### Statements vs. Expressions
Everything in Python is either a _statement_ or an _expression._ An expression has a value, and a statement does not. This is a subtle difference, do not spend too much time trying to grok this one if it doesn't come to you immediately. It isn't that important....yet.

Let's look at some examples. Consider the following code.
```python
x = 5 + 5
y = 123
```
Here, `5 + 5` is an _expression_ because it has a value, which is `10`. Once this expression is evaluated, the result (`10`) is stored in the _variable_ `x`. More trivial things are also expressions - `123` is an expression because it, too, has a value: `123`. 

But, then, what is a statement? A statement has _no value_. Consider the following **incorrect** code. 
```python
x = while True:
    print("foo")
```
This would not work, because `while` is a _statement_ and has no value, meaning there is nothing to store in `x`. In general, structurual keywords indicate statements. These include (don't worry if you don't recognize these yet):
- `for`
- `while`
- `def`
- `import`
- etc.

Consider the following snippet.
```python
let text = input()
if text == "hello":
    print("well, howdy")
else:
    print("why not say hello first?")
```
In this example, `if text == "hello"` [ ... ] `first?")` is a single _if-else statement_. 
