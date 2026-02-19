## Slide 1
A paragraph with some text and a [link](https://hakim.se).

---

## Slide 2

---

## Slide 3
```js [1-2|3|4]
let a = 1;
let b = 2;
let c = x => 1 + 2 + x;
c(3);
```

---

## Tuples
```python
t = (1, 2, 'Python', tuple(), (42, 'hi'))
```

---

- Tuples are the same as lists with the exception that the data once entered
into the tuple cannot be changed no matter what.
- The only exception is when the data inside the tuple is mutable, only then
can the data be changed.

---

## Tuple Manipulation
### Creating a Tuple

```python[1-3|5-7|9-11|13-15]
# Empty Tuple
my_tuple = ()
print(my_tuple)

# Tuple with integers
my_tuple = (1, 2, 3)
print(my_tuple)

# Tuple with mixed datatypes
my_tuple = (1, "Hello", 3.4)
print(my_tuple)

# Nested Tuple
my_tuple = ("mouse", [8, 4, 6], (1, 2, 3))
print(my_tuple)
```

>>>

test

>>>

---

test2