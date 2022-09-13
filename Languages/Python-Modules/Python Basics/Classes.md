# Classes

Object oriented programming languges like Python have objects. Almost everything in Python is an object, even the aforementioned types are objects. Classes are sort of constructors that create these objects. 

To create a class, one must use the keyword class.

```python
class MyClass:
	p = "ok"
```

Now we can use the class to create objects by calling it in our code.

```python
obj = MyClass()
print(obj.p) # This will print "ok"
```

The above are classes in the most simplest forms, not really applicable for most programs. 

All classes have a built in function called `__init__()`  which is executed when the class is being initiated. You generally use this function to assign values to class specific attributes.

```python
class Person:
	def __init__(self, name, age):
		self.name = name
		self.age = age

	def show_person(self):
		print(f"Hi, my name is {self.name} and I am {self.age} years old")

p1 = Person("John", 12)

print(p1.age)
print(p1.name)

p1.show_person()
```

Similar to function arguments, you can provide class arguments within the init function. I then convert them to class attributes by assigning the self parameter so that I may be able to use them elsewhere in the class.

In the class I also define a method named `show_person` which prints information regarding the person. Methods are functions but they belong to the class.

The self parameter is a reference to the current instance of the class and is used to access variables/methods that belong to the class. 

You can modify attributes like this

```python
p1.age = 30
```

You can delete properties with the `del` keyword

```python
del p1.name
```

You can delete entire objects with the `del` keyword

```python
del p1
```
