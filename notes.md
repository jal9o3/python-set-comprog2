
# Python Tuples
## Immutable Ordered Collections

---

## What is a Tuple?

A **tuple** is:
- An ordered collection
- Immutable (cannot be changed after creation)
- Allows duplicate values
- Can store mixed data types

Example:
```python
my_tuple = (1, 2, 3)
```

---

## Creating Tuples

### Basic Syntax

```python
numbers = (10, 20, 30)
```

### Without Parentheses (Tuple Packing)

```python
numbers = 10, 20, 30
```

### Single-Element Tuple (Important!)

```python
single = (5,)   # Comma is required!
```

---

## Tuple vs List

| Feature     | Tuple      | List            |
| ----------- | ---------- | --------------- |
| Mutable     | ❌ No       | ✅ Yes           |
| Syntax      | `( )`      | `[ ]`           |
| Performance | Faster     | Slightly slower |
| Use Case    | Fixed data | Changing data   |

---

## Accessing Tuple Elements

Tuples use **indexing**:

```python
colors = ("red", "green", "blue")

print(colors[0])  # red
print(colors[-1]) # blue
```

Indexing starts at `0`.

---

## Tuple Slicing

Extract a portion of a tuple:

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[1:4])  # (20, 30, 40)
```

Syntax:

```
tuple[start:end]
```

---

## Immutability Explained

Tuples **cannot be changed** after creation.

```python
numbers = (1, 2, 3)
numbers[0] = 10  # ❌ TypeError
```

This makes tuples:

* Safer for constant data
* Memory efficient

---

## Why Use Tuples?

Use tuples when:

* Data should not change
* Returning multiple values from functions
* Using data as dictionary keys
* Storing fixed configuration

---

## Tuple Packing & Unpacking

### Packing

```python
person = ("Alice", 25, "Engineer")
```

### Unpacking

```python
name, age, job = person
```

Each variable receives a corresponding value.

---

## Extended Unpacking

Using `*` operator:

```python
numbers = (1, 2, 3, 4, 5)

first, *middle, last = numbers
```

Results:

* `first = 1`
* `middle = [2, 3, 4]`
* `last = 5`

---

## Tuple Methods

Tuples have only **two built-in methods**:

```python
numbers = (1, 2, 2, 3)

numbers.count(2)   # 2
numbers.index(3)   # 3
```

Because tuples are immutable.

---

## Nested Tuples

Tuples can contain other tuples:

```python
matrix = (
    (1, 2),
    (3, 4)
)

print(matrix[0][1])  # 2
```

Useful for structured data.

---

## Converting Between List and Tuple

### Tuple → List

```python
numbers = (1, 2, 3)
numbers_list = list(numbers)
```

### List → Tuple

```python
numbers_tuple = tuple(numbers_list)
```

---

## Tuples as Dictionary Keys

Tuples can be used as dictionary keys because they are immutable.

```python
locations = {
    (40.7128, -74.0060): "New York",
    (34.0522, -118.2437): "Los Angeles"
}
```

Lists cannot be used as keys.

---

## Performance Benefits

Tuples:

* Use less memory
* Are faster to iterate
* Provide data integrity

---

## When in doubt:

Use a **tuple** for fixed data.
Use a **list** for changing data.

---

## Class Activity
1. Create a tuple with 5 values.
2. Unpack it into variables.
3. Slice the middle 3 elements.

