# `__str__`

This is useful if we want to use the instance of our class within a print statement.

Try run this code!

```python
class Person:
	def __init__(self, name, age):
		self.name = name
		self.age = age

	def __str__(self):
		return f"Name: {self.name}\nAge: {self.age}"

p1 = Person("Shell", 12)
print(p1)
```


