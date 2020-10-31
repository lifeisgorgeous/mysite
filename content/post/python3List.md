---
title: "Python3 Intermediates: List"
date: 2020-10-31T23:04:18+06:00
categories:
- Python
- Programming
tags:
- Python
- Programming
keywords:
- List
#thumbnailImage: //example.com/image.jpg
---

<!--more-->

```python
# List
```

# List Intermediate


```python
# Lists: ordered, mutable, allows duplicates elements

myList = ["banana", "cherry", "apple"]
print(myList)
```

    ['banana', 'cherry', 'apple']



```python
# Creating a list
```


```python
list_a = ["red", "green", "blue"]
print(list_a)

# Create an empty list
list_b = list()
print(list_b)

# Lists allow different data types
list_c = [10, "red", False]
print(list_c)

# Lists allow duplicates
list_d = ["green", "green", 15, 15]
print(list_d)
```

    ['red', 'green', 'blue']
    []
    [10, 'red', False]
    ['green', 'green', 15, 15]



```python
# Access elements
```


```python
item_1 = list_a[1]
print(item_1)

# Lists allow negative indexing
item_2 = list_a[-1]
print(item_2)
```

    green
    blue



```python
# Change Item
```


```python
# Lists can be altered
list_a[0] = "Orange"
print(list_a)
```

    ['Orange', 'green', 'blue']



```python
# Lists Methods
```


```python
new_list = ["Red", "Green", "Blue"]

# len(): get the number of elements in list
print("Length:", len(new_list))

# append(): adds an element to the end of the list
new_list.append("Orange")

# insert(): adds an element at the specified position
new_list.insert(1, "Violet")
print(new_list)


# pop(): removes and returns the item at the given position, default is the last item
item = new_list.pop()
print("Popped item: ", item)

# remove(): remove an item from the list
new_list.remove("Blue")
print(new_list)

# clear(): removes all items from the list
new_list.clear
print(new_list)

# reverse(): reverse the items
new_list = [1234, 1000, 4567, 7890, 2000, 500]
new_list.reverse()
print('Reversed: ', new_list)

# sort(): sort items in ascending order
new_list.sort()
print('Sorted: ', new_list)

# sorted(): to get a new list, and leave the original unaffected.
# It works on any iterable type

new_list = [1234, 1000, 4567, 7890, 2000, 500]
new_list = sorted(new_list)

# create list with repeated elements
list_with_greens = ["Green"] * 5
print(list_with_greens)

# Concatenations

list_concat = list_with_greens + new_list
print(list_concat)

# convert string to list
string_to_list = list('Yo Yo')
print(string_to_list)


```

    Length: 3
    ['Red', 'Violet', 'Green', 'Blue', 'Orange']
    Popped item:  Orange
    ['Red', 'Violet', 'Green']
    ['Red', 'Violet', 'Green']
    Reversed:  [500, 2000, 7890, 4567, 1000, 1234]
    Sorted:  [500, 1000, 1234, 2000, 4567, 7890]
    ['Green', 'Green', 'Green', 'Green', 'Green']
    ['Green', 'Green', 'Green', 'Green', 'Green', 500, 1000, 1234, 2000, 4567, 7890]
    ['Y', 'o', ' ', 'Y', 'o']



```python
# Copy a list

list_original = ["Red", "Green", "Blue"]

# To copy the reference to the list

list_copy = list_original

# Now, to modify the copy also affects the original
list_copy.append(True)
print("Original List: ", list_original)
print("Copied List: ", list_copy)

# To copy a list without affecting the original list, use copy() method or use list(x) or use slicing: list_copy = list_original[:]

list_original = ["Red", "Green", "Blue"]

list_copy1 = list_orginal.copy()
list_copy2 = list(list_original)
list_copy3 = list_original[:]

# Now we can modify the copied list without affecting the original one
list_copy1.append(True)
print("Copied List 1:", list_copy1)
list_copy2.append("False")
print("Copied List 2:",list_copy2)
list_copy3.append(100)
print("Copied List 3:",list_copy3)


```

    Original List:  ['Red', 'Green', 'Blue', True]
    Copied List:  ['Red', 'Green', 'Blue', True]
    Copied List 1: ['Red', 'Green', 'Blue', True]
    Copied List 2: ['Red', 'Green', 'Blue', 'False']
    Copied List 3: ['Red', 'Green', 'Blue', 100]


# Iterating


```python
# Iterating over a list by using a for in loop

for i in list_c:
    print(i)
```

    10
    red
    False



```python
# check if an item exists
```


```python
if "Red" in list_a:
    print("Yes.")
else:
    print("No.")
```

    No.



```python
# Slicing
# Access sub parts of the list with the used of colon(:)
```


```python
# a[start: stop: step], default step is 1

a = [10, 20 , 30, 40, 50, "Tom", "Jerry", "Charlie"]

# Slice from index 1 to index 4
b = a[1:4]
print(b)

# Until the end
b = a[3:]
print(b)

# From beginning
b = a[:5]
print(b)

# Replace a sub parts which is from index 0 to index 2
a[0:2] = [0]
print(a)

# Start to end with every second item
b = a[::2]
print(b)

# Reverse the list with a negative step
b = b[::-1]
print(b)

# Copy a list with slicing
b = a[:]
print(b)
```

    [20, 30, 40]
    [40, 50, 'Tom', 'Jerry', 'Charlie']
    [10, 20, 30, 40, 50]
    [0, 30, 40, 50, 'Tom', 'Jerry', 'Charlie']
    [0, 40, 'Tom', 'Charlie']
    ['Charlie', 'Tom', 40, 0]
    [0, 30, 40, 50, 'Tom', 'Jerry', 'Charlie']


# List comprehension

A way to create a new list from an existing list.


```python
new_list = [10, 20, 30 , 40, 50]
# Square each element
square_list = [i*i for i in new_list]
print(square_list)
```

    [100, 400, 900, 1600, 2500]



```python
# Nested lists
```


```python
new_list = [[10, 20], ["Red", "Green"]]
print(new_list)
print(new_list[1])
```

    [[10, 20], ['Red', 'Green']]
    ['Red', 'Green']



```python

```