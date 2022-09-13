# `__enter__ and __exit__`

Context managers are convenient blocks of code that essentially handle certain bits of code for you. 

Example of a context manager within built-in Python.

```python
with open("file.txt", "w") as f:
	f.write("ok")
```

This code here despite it being simple does a lot on the inside, you may think all it does is write ok to a file.

What it actually does is it first opens the file the minute you enter the with statement, then it executes your code. Which is to write "ok". Next it closes the file as you exit the context manager.

To accomplish something similar with your own classes you can do it like this.

```python
class Cars:

	def __init__(self, *cars):
	
		self.cars = cars
	
	  
	
	def __enter__(self):
	
		return print("Entered context manager")
	
	  
	
	def __exit__(self, exc_type, exc_val, exc_tb):
		
		return print("Exited context manager")

  

p = Cars("Audi", "BMW", "Penis")

  

with p:
	print("ok")
```

Essentially when you enter the with statement, the code in `__enter__` is executed. Then after printing "ok", the code in `__exit__` is executed.