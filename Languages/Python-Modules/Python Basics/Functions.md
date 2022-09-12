# Functions

Functions are pretty much blocks of code that are only ran when they are called. With functions you can also supply arguments/parameters that can be used within the function code. Here is an example of creating a function, and using it in code.

```python
def add_two(x):
	return x + 2

x = add_two(5)

print(x) # This will print 7
```

The function above takes the argument `x` and returns the value of `x + 2`. X in this case refers to an integer, if you passed a string to this function this would fail as you cannot add 2 to a string.

When you "return" a value, it means whatever is in the return statement in the function can be a variable. In the above function it means x + 2 or 5 + 2 is passed to the variable x. This is essentially the value 7. So when we print x is displays 7.

Here are a few more example functions

```python
def print_ten(msg):
	for i in range(10):
		print(msg)

print_ten("ok")
```

You can also have multiple arguments for a function

```python
def add(x, y):
	val = x + y
	return val

print(add(3,3)) # This will print 6
```

If the number of arguments are unknown you can add an asterisk in the arguments.

```python
def show_names(*names):
	for name in names:
		print(name)

show_names("john", "blake", "shell", "roover")
```

You can also create recursive functions. A recursive function is a function that calls itself, in most cases this is infinite and undesirable however, in some situations it is useful.

For example to find the factorial of a number, we have to multiply it by every number before it. Here is an example factorial function.

```python
def factorial(num):
	if num == 1:
		return 1
	else:
		return num * (factorial(num - 1))

print(factorial(5)) # This will print the factorial of 5 which is 120
```

The logic behind this function is as follows. If the number supplied is 1, it simply returns 1. Else it ends up multiplying num by the factorial of the number less than it by 1. Here is an example process of the logic

```
FACTORIAL OF 5

GREATER THAN 1

FACTORIAL OF 4

GREATER THAN 1

FACTORIAL OF 3

GREATER THAN 1

FACTORIAL OF 2

GREATER THAN 1

FACTORIAL OF 1

RETURNS 1 - here it ends up going back up the tree

RETURNS 1 * 2 - which is 2

RETURNS 2 * 3 - which is 6

RETURNS 6 * 4 - which is 24

RETURNS 24 * 5 - which is 120

RETURNS 120
```

*Sorry if my explanation is shit lmao*

