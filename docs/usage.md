## Importing
```python
from pyinverted import Inverted
```

## Creating a new object
```python
# Create/open a new inverted file
inv = Inverted('names')
```

## Inserting data
```python
inv.insert('PEANUT', 0)
inv.insert('PEANUT', 30)
inv.insert('PEANUT', 60)

inv.insert('BUTTER', 90)
inv.insert('BUTTER', 120)

# Change 'PEANUT' to 'HOMEMADE'
inv.update('PEANUT', 'HOMEMADE')
```

## Forcing file close and save
```python
# A representation of the object
inv_repr = repr(inv)

# Close file and save all
del inv
```

## Retrieving data
```python
# Get object from representation
inv = eval(inv_repr)

p = inv.get('PEANUT')    # empty list
h = inv.get('HOMEMADE')  # [0, 30, 60]
b = inv.get('BUTTER')    # [90, 120]
```

## Deleting data
```python
inv.delete('BUTTER', 90)
h = inv.get('BUTTER')    # [120]

inv.delete('BUTTER', 120)
h = inv.get('BUTTER')    # []
```
