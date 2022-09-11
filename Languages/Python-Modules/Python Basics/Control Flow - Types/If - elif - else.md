# If statements
If statements are a sort of statement where if a certain condition is regarded to be True, code will run. Here is an example.

```python
age = 12

if age > 18:
	print("Allowed to drink")
```

This code here will not do anything since the condition of `age > 18` is not met. Therefore the program will simply stop running. However what if we wanted to say some sort of message before it stopped running, like "You need to be 18 to drink". Here we can use the else statement.

The else statement comes after the if statement. It is only ran if all the conditions are false.

```python 
age = 12

if age >= 18:
	print("Allowed to drink")
else:
	print("You are too young. You need to be 18 to drink sir.") # This will print
```

However, say if you want to check multiple different conditions, how would you do that? In discord you are required to be 13 to use the platform, however required to be 18 to see NSFW images. If you are under 13 you are not allowed to use the platform. In this situation we will be using the elif statement.

```python
age = 14

if age >= 13:
	print("Allowed to be on this platform") # This will only print
elif age >= 18:
	print("Allowed to see NSFW images")
else:
	print("Not allowed to be on this platform")
```

In this scenario only the first condition is met, however the elif condition is not met therefore this will not run. The else statement will not run since the first if condition is true.

You can have many if and elif statements, however there can only be one else statement situated at the end.

*I can't lie I don't think I explained this well lmao*
