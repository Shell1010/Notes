# [Asyncio tasks](https://docs.python.org/3/library/asyncio-task.html#asyncio.create_task)

  

Asyncio tasks are high level, light, non-blocking units of execution known tasks. They are essentially what asyncio uses to run tasks in the background concurrently. This allows main thread to do something while the task is in the background working. Here is an example:

  

```python

import asyncio

import time

async def say_after(delay, msg):

await asyncio.sleep(delay)

print(msg)

async def main():

print(f"Started at {time.strftime('%X')}")

task1 = asyncio.create_task(say_after(1, "Task 1 finished"))

task2 = asyncio.create_task(say_after(2, "Task 2 finished"))

await task1

await task2

print(f"Finished at {time.strftime('%X')}")

```

  

The following code will finish itself after 2 seconds, rather than waiting 3 seconds due to the fact each task is executed in the background.