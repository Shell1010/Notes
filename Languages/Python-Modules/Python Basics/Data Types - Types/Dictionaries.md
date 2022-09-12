# Dictionaries

Dictionaries are a type of data which holds key value pairs. It's perhaps one of the more complex data types of python. This is an example of one.

```python
var = { "name": "John", "age": 12, "location": "England"}
```

The key of every dictionary is a string, for the above dictionary, the keys are name, age and location. After each key comes a colon, and after it will dictate the value associated to the key. So the key `name` has the value `John`. The key `age` has the value `12`.  The key `location` has the value `England`. Each key-value pair is seperated using a comma.

To add a key-value pair to a dictionary one needs to do this.

```python
var = { "name": "John", "age": 12, "location": "England"}

var["hobbies"] = "Gaming"

print(var) # This will now print {"name": "John", "age": 12, "location": "England", "hobbies": "Gaming"}
```

The key `hobbies` is given the value `Gaming` and added to the dictionary. For context, you can add any sort of data type to a dictionary value.

If you would like to modify a particular keys value, you can do this.

```python
var = { "name": "John", "age": 12, "location": "England"}
var["location"] = "Germany"
print(var) # This will now print { "name": "John", "age": 12, "location": "Germany"}
```

To check how many items are in a dictionary, you can use the `len()` [function](Functions).

```python
var = { "name": "John", "age": 12, "location": "England"}
print(len(var)) # This will print 3
```

To get all the keys in a particular dictionary you can use the `keys()` method.

```python
var = { "name": "John", "age": 12, "location": "England"}
print(var.keys()) # This will print ["name", "age", "location"]
```

To get all the values in a particular dictionary you can use the `values()` method.

```python
var = { "name": "John", "age": 12, "location": "England"}
print(var.values()) # This will print ["John", 12, "England"]
```

To remove a particular item from a dictionary you can use the `pop()` method.

```python
var = { "name": "John", "age": 12, "location": "England"}
var.pop("name")
print(var) # This will print {"age": 12, "location": "England"}
```