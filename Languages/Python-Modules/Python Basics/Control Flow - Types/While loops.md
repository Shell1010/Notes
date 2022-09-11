# While loops

While loops are executed as long as a certain condition is met. You may use [[Comparison Operators]] to achieve this. Example.

```python
var = 12

while var < 18:
	print("Still in loop")
	var += 1 # This is equivalent to var = var + 1

print("Finished loop")
```

Unlike most other loops you have to manually handle the condition, else the loop will run forever. So in this case I am incrementing var by 1 each time the loop is ran. 

To make a loop run forever, you just need to make sure a condition is always True. So in this case all you need to do is this.

```python
while True:
	print("This runs forever!")
```

Similar to [[For loops]] you have break statements. This allows you to exit the loop, you can execute this if a certain condition is met.

```python
var = 12

while var < 18:
	print("Still in loop")
	var += 1 # This is equivalent to var = var + 1
	if var == 15:
		break

print("Finished loop")
```

Similar to [[For loops]] you can have continue statements. This allows you to skip the current iteration and go to the next. You can execute this if a certain condition is met.

```python
var = 12
while var < 18:
	print(var)
	var += 1
	if var == 15:
		continue
		
print("Finished loop")
```