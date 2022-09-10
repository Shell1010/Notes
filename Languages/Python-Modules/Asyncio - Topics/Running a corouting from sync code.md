# [Running a coroutine from sync code](https://docs.python.org/3/library/asyncio-task.html#running-an-asyncio-program)

I am writing this out for just organisations sake. As stated earlier, the only way to call an async function from sync code is using the `asyncio.run` function. This is a function that allows you to run a coroutine via asyncio.

```python
import asyncio

async def main():
	print("ok")

asyncio.run(main())
```
