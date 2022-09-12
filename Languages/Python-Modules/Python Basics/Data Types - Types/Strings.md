# Strings

This here is a string. It is a data type that is generally used to represent text.

```python
var = "This is a string"
```

Do note that a string containing a number is not regarded an [integer](Integers), therefore you cannot use this for mathematical operations.

```python
string = "2"
number = 2

val = string + number # This here would give an error

"""
Traceback (most recent call last):  
 File "<stdin>", line 1, in <module>  
TypeError: unsupported operand type(s) for +: 'int' and 'str'
"""
```

You can define multiline strings like this.

```python
var = """This is how
you can
do it"""
print(var)
```

Strings are quite similar to arrays in the fact that each character holds an index, the index always starts at 0. In fact in most languages, strings are deemed to be an array of characters.

```python
var = "Hello Shell"

print(var[0]) # This will print "H"
```

Since strings are deemed an array, they can be looped through.

```python
var = "Shell"

for char in var:
	print(char)
	
# This will print each character in the string one by one

```

To check if a string is present in another string you can use if statements like this.

```python
var = "Hello my name is shell"
if "Shell" in var:
	print("ITS HERE")
```

To check the length of a string use the `len()` [function](Functions).

```python
var = "Shell"
print(len(var)) # This will print 5
```
