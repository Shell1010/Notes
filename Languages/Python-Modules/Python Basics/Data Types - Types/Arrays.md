# Arrays

Arrays are a list of data. They can contain several [[Data Types]], or the same data type. This is an Array.

```python
var = ["word", 123, 2.5]
```

Arrays by default can hold infinite amounts of data (or as much as your memory can take). Each item in an array is seperated by a comma, in order to call a specific item in an array, you call the index. As stated in the [[Strings]] section, index begins at 0 for arrays.

```python
var = ["test", "other", "word"]
print(var[0]) # This will print "test"
print(var[1]) # This will print "other"
```

In order to push an item to an already initialised (created) array, you can use the `push()` method.

```python
list = ["ok", "ok", 1, 2]

list.push(5)

print(list) # This will print ["ok", "ok", 1, 2, 5]
```

In order to delete a specific element by value from the list you can use the `remove()` method. Here is an example.

```python
list = [0,1,2,3,4,5]
list.remove(3)
print(list) # This will print [0,1,2,4,5]
```

In order to delete a specific element by index from the list you can use the `pop()` method. This method also returns the removed value.

```python
list = [1,2,3,4,5]
val = list.pop(0)
print(val) # This will print 1
print(list) # This will print [2,3,4,5]
```

