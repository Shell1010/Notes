# [Awaitables](https://docs.python.org/3/library/asyncio-task.html#id2)

In asyncio, anything that is described as an **awaitable** object can be used within an await expression. E.g  `await balls` . The two main awaitables are [[Asyncio Tasks]] and [[Coroutines]], there are also futures, which are more low-level and not recommended to be used unless you have to.