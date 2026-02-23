# Python Sets
### A Complete Lesson (20 Slides)

---

## 1. Introduction to Python Sets

- Sets are **unordered**, mutable collections of **unique elements**
- Defined using `{}` or the `set()` constructor
- Built-in Python data type
- Ideal for membership testing and removing duplicates

---

## 2. Why Use Sets?

- Automatically remove duplicate values
- Fast membership testing (average **O(1)**)
- Support mathematical set operations
- Useful in data cleaning and filtering

---

## 3. Creating Sets

```python
# Using curly braces
s1 = {1, 2, 3}

# Using set() constructor
s2 = set([1, 2, 3])

# Empty set (correct way)
empty = set()
```

> `{}` creates an empty dictionary, not a set.

---

## 4. Set Characteristics

* Unordered (no indexing)
* Mutable (can add/remove elements)
* No duplicate elements
* Elements must be **hashable**

---

## 5. Valid Set Elements

**Allowed:**

* `int`, `float`, `str`
* `tuple` (if immutable)

**Not allowed:**

* `list`, `dict`, `set`

```python
valid = {1, "hello", (1, 2)}
```

---

## 6. Removing Duplicates Example

```python
numbers = [1, 2, 2, 3, 4, 4]
unique_numbers = set(numbers)
print(unique_numbers)
```

* Converts list to unique elements
* Order is not preserved

---

## 7. Adding Elements

```python
s = {1, 2, 3}
s.add(4)
```

* `add()` inserts one element
* No effect if element already exists

---

## 8. Updating Sets

```python
s = {1, 2}
s.update([3, 4])
```

* `update()` adds multiple elements
* Accepts any iterable

---

## 9. Removing Elements

```python
s.remove(2)     # Raises error if not found
s.discard(3)    # No error if not found
s.pop()         # Removes arbitrary element
s.clear()       # Empties the set
```

---

## 10. Membership Testing

```python
if 2 in s:
    print("Found")
```

* Extremely efficient (hash-based lookup)
* Faster than list membership testing

---

## 11. Set Operations Overview

Sets support mathematical operations:

* Union
* Intersection
* Difference
* Symmetric Difference

---

## 12. Union

```python
a = {1, 2, 3}
b = {3, 4, 5}

a | b
a.union(b)
```

Result:

```python
{1, 2, 3, 4, 5}
```

---

## 13. Intersection

```python
a & b
a.intersection(b)
```

Result:

```python
{3}
```

* Elements common to both sets

---

## 14. Difference

```python
a - b
a.difference(b)
```

* Elements in `a` but not in `b`

---

## 15. Symmetric Difference

```python
a ^ b
a.symmetric_difference(b)
```

* Elements in either set, but not both

---

## 16. Subset and Superset

```python
a = {1, 2}
b = {1, 2, 3}

a.issubset(b)
b.issuperset(a)
```

Operators:

```python
a <= b
b >= a
```

---

## 17. Frozen Sets

* Immutable version of a set
* Created with `frozenset()`

```python
fs = frozenset([1, 2, 3])
```

* Can be used as dictionary keys
* Cannot add/remove elements

---

## 18. Set Comprehensions

```python
squares = {x**2 for x in range(5)}
```

* Similar to list comprehensions
* Produces a set

---

## 19. Performance Considerations

* Membership test: **O(1)** average
* Union/intersection: **O(len(s) + len(t))**
* Implemented using hash tables
* Not suitable when order matters

---

## 20. Practical Use Cases

* Removing duplicates
* Finding common elements between datasets
* Tracking unique visitors
* Graph algorithms (visited nodes)
* Access control lists and permissions

---

# Questions?