# For loops

For loops are used for iterating over a sequence, like [list](Arrays), [dictionary](Dictionaries), or [string](Strings). Generally you'd want to use a for loop if you know how many times you are going to iterate over something.

```python
for i in range(10):
	print("ok")

# This will print "ok" 10 times
```

You can use the `range()` function to dictate easily how many times you want to run something. It returns a sequence of numbers, starting from 0 by default and increments by 1. So essentially this loop will run 10 times.

However if you print the value i...

```python
for i in range(10):
	print(i)
```

```Output
0  
1  
2  
3  
4  
5  
6  
7  
8  
9
```

Essentially runs 10 times, but since the sequence starts at 0 and not at 1, we only reach 9.

You can use for loops to iterate over each item in a [list](Arrays). Same with [[Strings]].

```python
var = ["apple", "feet", "hands"]
for item in var:
	print(item)

# This will print each item in the list one by one
```

You can use a `break` statement to exit the loop, this can be activated if a certain condition is met.

```python
var = ["apple", "feet", "hands"]
for item in var:
	if item == "feet":
		break
	print(item)

print("Outside the loop")

# This will only print "apple" and then will print "Outside the loop"
```

This is because when feet is reached, the loop is broken and the code outside the loop is then executed.

You can use a `continue` statement to sort of skip the current iteration and go onto the next. This can be executed if a certain condition is met.

```python
var = ["apple", "feet", "hands"]
for item in var:
	if item == "feet":
		continue
	print(item)

# This will only print "apple" and "hands" and NOT print "feet"
```

You can use `else` statements alongside for loops. These statements will only run if the loop is finished. Do note, the else statement will not run if you stop the loop using the `break` statement.

```python
for i in range(10):
	print(i)
else:
	print("Finished")
```