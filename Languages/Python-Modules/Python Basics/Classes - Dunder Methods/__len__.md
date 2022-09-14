# `__len__`

This is a special type of method that is invoked when you call the `len()` function.

```python
class Cars:
	def __init__(self, *cars):
		self.cars = cars

	def __len__(self):
		return len(self.cars)

p = Cars("Audi", "BMW", "Penis")

print(len(p))
```

In this case, our len dunder method is returning the amount of cars.