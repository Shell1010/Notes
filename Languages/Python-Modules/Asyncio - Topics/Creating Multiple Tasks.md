# [Creating multiple tasks](https://docs.python.org/3/library/asyncio-task.html#asyncio.create_task)

```python
async def main():
	for i in range(100):
		asyncio.create_task(do_something())
	# This will execute all 100 tasks in the background
	# Your main thread has to be doing something else the program will close itself
	for i in range(10000):
		print("Ok")
	
```
