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

### Creating a Tuple without Parentheses
#### a.k.a. Tuple Packing
```python[1|6|3-4|7-8]
my_tuple = 3, 4.6, "dog"

# Tuple Unpacking is also possible
a, b, c = my_tuple

print(a) # 3
print(b) # 4.6
print(c) # dog
```

>>>

## Creating a Tuple with One Element
```python[1-2|4-6|8-10]
my_tuple = ("hello")
print(type(my_tuple)) # <class 'str'>

# Creating a tuple with one element
my_tuple = ("hello",)
print(type(my_tuple)) # <class 'tuple'>

# Parenthesis is optional
my_tuple = "hello",
print(type(my_tuple)) # <class 'tuple'>
```
- When creating a tuple with one element, you need to put a trailing coma.

>>>

## Accessing Multiple Elements: Indexing

```python[1-2|4|5|7-8|10-11|13-14|16-18]
# Accessing tuple elements using indexing
my_tuple = ('p', 'e', 'r', 'm', 'i', 't')

print(my_tuple[0]) # 'p'
print(my_tuple[5]) # 't'

print(my_tuple[6]) 
# IndexError: list index out of range

my_tuple[2.0] 
# TypeError: list indices must be integers, not float

# Nested Tuple
n_tuple = ("mouse", [8, 4, 6], (1, 2, 3))

# Nested Index
print(n_tuple[0][3]) # 's'
print(n_tuple[1][1]) #  4
```

>>>

## Accessing Tuple Elements: Negative Indexing
```python[1-2|4|6]
# Negative indexing for accessing tuple elements
my_tuple = ('p', 'e', 'r', 'm', 'i', 't')

print(my_tuple[-1]) # 't'

print(my_tuple[-6]) # 'p'

```

>>>

## Accessing Tuple Elements: Slicing

```python[1-2|4-5|7-8|10-11|13-14]
# Accessing tuple elements using slicing
my_tuple = ('p', 'r', 'o', 'g', 'r', 'a', 'm')

# Accessing the 2nd to 4th elements
print(my_tuple[1:4]) # ('r', 'o', 'g')

# Accessing starting from the 1st to 2nd element
print(my_tuple[:-5]) # ('p', 'r')

# Accessing elements from the 5th element to the end
print(my_tuple[4:]) # ('r', 'a', 'm')

# Accessing all elements from the first to the last
print(my_tuple[:]) # ('p', 'r', 'o', 'g', 'r', 'a', 'm')
```

>>>

---