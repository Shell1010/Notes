# [Coroutines](https://docs.python.org/3/glossary.html#term-coroutine)

Coroutines declared with the async/await syntax is the way of writing async applications within python. To declare a coroutine, one must write a function, but add the async keyword to the start of it.

```python
import asyncio

async def main():
	print("hello")
	await asyncio.sleep(3)
	print("Slept for three seconds")

asyncio.run(main())
	
```

This snippet of code prints "hello", then waits three seconds, and afterwards prints "Slept for three seconds". 

Do note that simply calling a coroutine like a regular function will not execute the coroutine.

```python
main()
```

To actually run coroutines, asyncio provides three main ways to run them:
- asyncio.run() - This is essentially the top-level entrypoint, what the main() function which holds all your code should be ran under. It's the only way to execute a coroutine in a non-async environment.
- awaiting a coroutine - This is how one is able to run coroutines within async functions, one is able to await them. Here is an example:

```python
import asyncio

async def say(msg: str):
	await asyncio.sleep(1)
	print(msg)

async def main():
	print("Hello")
	await say("This is how you execute a coroutine in an async function")
	await say("It's pretty cool")
	await asyncio.sleep(1)
```
