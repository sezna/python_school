# Functions
We are finally going to sit down and figure out what the heck a _function_ actually is. You have already used two: `exit()` and `input()`. But why are there parenthesis after them? What do they mean?

When we use a function, it is called "calling" a function. A function call consists of two parts: the name of the function, and the arguments that the function will use. The arguments of the function are contained within the parenthesis. Let's learn a new function and use it as an example. `len` is the name of a function which takes a single argument and counts the _length_ of it. Here are some example callings of `len`:
* `len("hello")` is `5`
* `len("austin")` is `6`
* `len("")` is `0`
Note that the name of the function, _len_, is immediately followed by a single argument, which is a _string_. The argument is contained within parenthesis.

If a function takes zero arguments, then the parenthesis are empty. This is what is happening in the case of `exit()` and `input()`. Yes, they are functions, but they don't need any arguments to work.

But what is a function useful for? Why does this weird parenthesis thing exist?

A function takes a single functionality and performs it in a repeatable way. For example, in one of our earlier projects, we defined a function called `add`. It took two arguments, which were numbers, and added the together. Calling `add` looked like this:
```python
add(5, 5) # 10
add(3, 2) # 5
add(0, 0) # 0
```

Note that when a function has multiple arguments, they're separated by a comma.

# Function Composition
_Function Compos-what?_ -- yes, we are finally learning things with cool names. Cool names are all over computer science. Eventually, we will learn _polymorphism_, _abstract data interfaces_, _genetic algorithms_, _neural networks_, and _polyrhythms_...wait, no, not that last one.

Function composition is when you use one function as the input to another function. You've actually already done this -- look at your calculator you wrote. There's a line that looks something like this:
```python
x = int(input())
```

You are calling the function `input()` and its output becomes the input of the `int()` function. If you remember algebra, this is also function composition:
```
f(x) = x + 1
g(x) = x - 1
f(g(x)) = x
```
Here, `f(g(x))` is passing the output of the function `g(x)` as the input into the function `f(x)`. Remember, parenthesis are evaluated from the innermost to the outermost.

So, remembering our `add()` function, we could actually use _function composition_ to compose it even more. Behold
```python
print(add(int(input()), int(input())))
```
If you need to take a cold shower after looking at that, you might be interested in the nerdy pasttime of _code golf_, or solving a problem in the least amount of characters possible.

We are just going to cover using functions this week. We can talk about creating functions yourself next time.

# Vim Stuff
Let's review the vim stuff we covered.
* shift+v, or just `V` - highlight an entire line at a time.
* yank/paste - `y` and `p` - copy and paste
* `dd` - cut the current line (can be pasted with `p`)
* `yy` - copy the current line (can be pasted with `p`)

# Exercise
Create a python file which takes input from a user and, if it has a length (remember `len()` -- _hint hint_ `len(input())` of greater than 5, print "i don't know any words that long". Otherwise, print "Hey, I know that word!"
