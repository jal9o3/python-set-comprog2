## Lesson V  
# Python Sets  
### Unique Unordered Collections  

Jerome Loria  
February 2026

---

## What are Sets?

- Unordered, mutable collections of unique elements  
- Defined with `set()`  
- Built-in Python data type  
- Great for membership testing and deduplication  

---

## Creating Sets

```python
# Using curly braces
s1 = {1, 2, 3}

# Using set() constructor
s2 = set([1, 2, 3])

# Empty set (correct way)
empty = set()
```

`{}` creates an empty dictionary, not a set.

---

## Set Characteristics

* Unordered (no indexing)
* Mutable (can add/remove elements)
* No duplicate elements

---

## Valid Set Elements

**Allowed:** `int`, `float`, `str`, `tuple`

**Not allowed:** `list`, `dict`, `set`

```python
valid = {1, "hello", (1, 2)}
```

---

## Removing Duplicates

```python
numbers = [1, 2, 2, 3, 4, 4]
unique_numbers = set(numbers)
print(unique_numbers)
```

* Converts a list into unique elements
* Order is not preserved

---

## Adding Elements

```python
s = {1, 2, 3}
s.add(4)
```

* `add()` inserts one element
* No effect if the element already exists

---

## Updating Sets

```python
s = {1, 2}
s.update([3, 4])
```

* `update()` adds multiple elements
* Accepts any iterable

---

## Removing Elements

```python
s.remove(2)     # Raises error if not found
s.discard(3)    # No error if not found
s.pop()         # Removes arbitrary element
s.clear()       # Empties the set
```

---

## Membership Testing

```python
if 2 in s:
    print("Found")
```

---

## Set Operations Overview

Sets support mathematical operations:

* Union
* Intersection
* Difference
* Symmetric Difference

---

## Union

```python
a = {1, 2, 3}
b = {3, 4, 5}

a | b
a.union(b)

# {1, 2, 3, 4, 5}
```

---

## Intersection

```python
a & b
a.intersection(b)

# {3}
```

Elements common to both sets.

---

## Difference

```python
a - b
a.difference(b)
```

Elements in `a` but not in `b`.

---

## Symmetric Difference

```python
a ^ b
a.symmetric_difference(b)
```

Elements in either set, but not both.

---

## Subset and Superset

```python
a = {1, 2}
b = {1, 2, 3}

a.issubset(b)
b.issuperset(a)

a <= b
b >= a
```

---

## Frozen Sets

```python
fs = frozenset([1, 2, 3])
```

* Immutable version of a set
* Can be used as dictionary keys
* Cannot add or remove elements

---

## Set Comprehensions

```python
squares = {x**2 for x in range(5)}
```

* Similar to list comprehensions
* Produces a set directly

---

## Practical Use Cases

* Removing duplicates
* Finding common elements between datasets
* Tracking unique visitors
