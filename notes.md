# Lesson IV
## Python Tuples
### Immutable Ordered Collections

Jerome Loria — February 2026

---

## What is a Tuple?

- An ordered collection
- Allows duplicate values
- Can store mixed data types
- Immutable (cannot be changed after creation)

---

Tuples look like this:

```python
my_tuple = (1, 2, 3)
```

---

## Creating Tuples

#### Basic Syntax
```python
numbers = (10, 20, 30)
```

#### Tuple Packing
```python
numbers = 10, 20, 30
```

#### Single-Element Tuple
```python
single = (5,)   # Comma is required!
```

---

## Tuple != Parentheses

```python
a = (1, 2, 3)
b = 1, 2, 3

print(type(a))  # tuple
print(type(b))  # tuple
```

**The comma**, not the parentheses, creates a tuple.

---

## Parentheses for Clarity

Parentheses are optional, but they are recommended for:

- Readability
- Preventing ambiguity
- Multi-line formatting

```python
coordinates = (
    40.7128,
    -74.0060
)
```

---

## Single-Element Tuple Rule

Common mistake:
```python
single = (5)
print(type(single))  # int
```

Correct:
```python
single = (5,)
print(type(single))  # tuple
```

---

## Empty Tuples

Correct syntax:
```python
empty = ()
```

Invalid syntax:
```python
empty = ,   # SyntaxError
```

---

## Tuple Creation from Iterables

```python
numbers = tuple([1, 2, 3])
letters = tuple("abc")

print(numbers)  # (1, 2, 3)
print(letters)  # ('a', 'b', 'c')
```

---

## List and Tuple Conversion

#### Tuple → List
```python
numbers = (1, 2, 3)
numbers_list = list(numbers)
```

#### List → Tuple
```python
numbers_tuple = tuple(numbers_list)
```

---

## Trailing Commas

```python
values = (1, 2, 3,)
```

- Easier element additions
- Valid and recommended in long tuples

---

## Nested Tuple Creation

```python
data = (
    ("Alice", 25),
    ("Bob", 30),
    ("Charlie", 35)
)
```

Useful for structured immutable records.

---

## Packing & Returns

```python
def get_user():
    return "Alice", 25

result = get_user()
print(result)  # ('Alice', 25)
```

Python automatically packs return values into a tuple.

---

## Tuple Creation with Generators

```python
squares = tuple(x**2 for x in range(5))
print(squares)  # (0, 1, 4, 9, 16)
```

The generator expression is consumed by `tuple()`.

---

## Accessing Tuple Elements

```python
colors = ("red", "green", "blue")

print(colors[0])  # red
print(colors[-1]) # blue
```

Indexing starts at **0**.

---

## Tuple Slicing

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[1:4])  # (20, 30, 40)
```

Format:
```python
tuple[start:end]
```

---

## Tuple Packing & Unpacking

#### Packing
```python
person = ("Alice", 25, "Engineer")
```

#### Unpacking
```python
name, age, job = person
```

---

## Tuples as Dictionary Keys

```python
locations = {
    (40.7128, -74.0060): "New York",
    (34.0522, -118.2437): "Los Angeles"
}
```

Lists cannot be used as keys, **but tuples can be.**

---

## When To Use Which

Use a **tuple** for fixed data.

Use a **list** for changing data.

---

## Class Practice

1. Create a tuple with 5 values.
2. Unpack it into variables.
3. Slice the middle 3 elements.