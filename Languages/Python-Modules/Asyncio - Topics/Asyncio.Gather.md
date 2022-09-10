# [Asyncio.gather](https://docs.python.org/3/library/asyncio-task.html#running-tasks-concurrently)

Asyncio.gather is a type of coroutine that allows you to run many different awaitables concurrently alongside each other. If all the awaitables are completed successfully, it will return a list of returned values from it. 

If return_exceptions is True, the exceptions are treated the same as successful results and will be aggregated into the list, if you didn't handle exceptions this will most likely return None.

```python
async def main():
	tasks = []
	for i in range(100):
		task = asyncio.create_task(do_something(i))
		tasks.append(task)
		
	vals = await asyncio.gather(*tasks)
	print(vals)
```

Or alternatively this does the same thing...

```python
async def main():
	vals = await asyncio.gather(*(asyncio.create_task(do_something(i)) for i in range(100)))
	print(vals)

```
