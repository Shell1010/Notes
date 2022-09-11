# Floats

Similar to [integers](Integers), floats are also numbers, but they are decimal. This here is a float type.

```python
var = 2.5
```

You can do math with floats.

```python
var = 2.5
other_var = 3.1

print(var + other_var) # This will print 5.6
```

Here is the complete list of arithmetic operators within Python.

| Operator | Name           | Description           | Example | Result |
| -------- | -------------- | --------------------- | ------- | ------ |
| +        | Add            | Adds numbers          | 2 + 3   | 5      |
| -        | Subtract       | Subtracts numbers     | 5 - 2   | 3      |
| *        | Multiply       | Multiplies numbers    | 5 * 2   | 10     |
| /        | Divide         | Divides numbers       | 6 / 2   | 3      |
| **       | Exponentiation | Exponentiates numbers | 5 ** 2  | 25     |
| //       | Floor Division | Floor Divides numbers | 15 // 4 | 3      |
| %        | Modulos        | Modulos numbers       | 12 % 5  | 2      |         |                |                       |         |        |


With floats you can also use comparison operators to determine whether a condition is true/false. For example.

```python
var = 2.5

if var < 3:
	print("OK")
else:
	print("Fail")
```

Here is the complete list of comparison operators within Python.

| Operator | Name                     | Example | Result |
| -------- | ------------------------ | ------- | ------ |
| ==       | Equal to                 | 5 == 5  | True   |
| !=       | Not equal to             | 5 != 5  | False  |
| >        | Greater than             | 5 > 3   | True   |
| >=       | Greater than or equal to | 5 >= 6  | False  |
| <        | Less than                | 5 < 6   | True   |
| <=       | Less than or equal to    | 6 <= 6  | True   |
|          |                          |         |        |

Mathematical operations/comparison operations between floats and [integers](Intergers) works also.

```python
var = 2.5
other_var = 2
print(var + other_var) # This will print 4.5
```