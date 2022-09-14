# Iterators

Iterators are objects that can be cycled through. We've covered a few of these already, which are strings, arrays and dictionaries.

We can use the `__iter__` and `__next__` methods in our classes to build a custom iterator if required. 

```python
class Cars:

	def __init__(self, *cars):
	
		self.cars = cars
		
		self.max = len(self.cars) - 1
	
	  
	
	def __iter__(self):
	
		self.n = 0
		
		return self
	
	  
	
	def __next__(self):
	
		if self.n <= self.max:
		
			result = self.cars[self.n]
			
			self.n += 1
			
			return result
		
		else:
		
			raise StopIteration


p = Cars("Audi", "BMW", "Penis")

for i in p:

	print(i)
```

Here when we initialise the class we set the cars attribute. And we also set the max attribute. The max attribute in this case is the amount of cars -1. This is because we are going to be calling values in the list cars through the index, and since indexes start at 0, we need to deduct 1.

We then create the `__iter__` func, this sets a variable known as self.n to 0. 
