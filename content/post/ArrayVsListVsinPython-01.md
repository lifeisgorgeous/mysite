---
title: "Data Structures Using Python: Array Based-Sequences [Part -1]"
description: "Array Vs List Vs Tupple"
date: 2020-08-24T23:22:47+06:00
thumbnailImagePosition: right
categories:
- Programming 
- Python
- Data Structure
tags:
- Programming 
- Python
keywords:
- Array
- List
- Tuple
- Python
thumbnailImage: https://res.cloudinary.com/ddlohuyww/image/upload/c_crop,h_400,w_400/v1598290385/images/18705_iimcyw.png
thumbnailImage: https://res.cloudinary.com/ddlohuyww/image/upload/v1598290385/images/18705_iimcyw.png
coverImage: https://res.cloudinary.com/ddlohuyww/image/upload/v1598290385/images/18705_iimcyw.png
metaAlignment: center
coverCaption: "Photo by pressfoto"
---

<!--more-->

### Array V/s List V/s Tupple 

I started to explore the uses of the data structures more in-depth in Python. Suddenly, a question stuck in my mind that can we use a list in replace of an array in Python. Then I started a little research from books and over the Internet and tried to tie up what I learn in this blog.

**Note**: In Python, we write programs from an abstraction level, that’s why it’s also called high-level programming language that means Python is more human-readable code than machine-readable. To understand the core concept of an Array-based sequence more in-depth, in Part 2 of this blog we will discuss the concept of the low-level array and dynamic array class in Python. I will try to write more relevant details of those concepts in the next part very soon! This blog may not be helpful for very beginners in programming. For whom it may concern, who knows Python or any other programming language or the basics of programming let’s dive deeper into the similarities and differences between Array, List, and Tuple using Python!

###  Revision: What is an Array?

An array is a data structure and a collection of elements of the same type. The elements are referenced by their index. For N elements index is started from 0 to N - 1. 

We can do append, remove, and modify operations on an Array.

In Python, arrays are ordered, mutable, and can be stored as non-unique items. 

There are two ways to use an Array in Python: 

**i) Importing by Array module:**

{{< codeblock "arrayExample.py" "python">}}

import array as arr

TopTen = arr.array("i",[10,20,30,40,50,60,70,80,90,100])

print(TopTen) 

{{< /codeblock >}}

```
Output: array('i', [10, 20, 30, 40, 50, 60, 70, 80, 90, 100])
```

We imported the array module and named it arr. After that, we have created a variable called TopTen where we created an array of ten elements, and "i" represents that they are integers. 

To see the type of the `TopTen` type: 

{{< codeblock  "arrayExample.py">}}

print(type(TopTen))

{{< /codeblock >}}

```
Output : <class 'array.array'>
```

Let's see some operations on `TopTen` array:

{{< codeblock  "arrayOperationExample.py">}}

#To see the length in bytes of one array item in the internal representation

TopTen.itemsize     # Output: 4

#To append or add a new item to the end of the array

TopTen.append(110)    # array('i', [10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110])

#To see the number of a element appears to an array

TopTen.count(110)    # Output: 1

#To return index no. of the first occurrence of a value in the array 

TopTen.index(100)  # Output: 9

#To insert an element into an specific index

TopTen.insert(2, 120)   # array('i', [10, 20, 120, 30, 40, 50, 60, 70, 80, 90, 100, 110])

#To remove the item with the index i from the array and returns it.

TopTen.pop(2)    # Element '120' removed. array('i', [10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110])

#To remove an element from an array

TopTen.remove(30)    # array('i', [10, 20, 40, 50, 60, 70, 80, 90, 100, 110])

#To reverse an element

TopTen.reverse()     # array('i', [110, 100, 90, 80, 70, 60, 50, 40, 20, 10])

#To convert the array to an ordinary list with the same items

TopTen.tolist()    # [110, 100, 90, 80, 70, 60, 50, 40, 20, 10]

{{< /codeblock >}}

**ii) Importing by NumPy Packages:**

{{< codeblock  "numpyExample.py">}}

import numpy as np

TopTenNP = np.array([10,'Twenty',30,'Forty',50,60,'Seventy',80,'Ninty',100])

print(TopTenNP)

{{< /codeblock >}}

```
Output: ['10' 'Twenty' '30' 'Forty' '50' '60' 'Seventy' '80' 'Ninty' '100']
```

In the code snippets we can see that, we imported the NumPy package and named it np. Then we took a variable named ToptenNP and assigned some elements in different data types. Yes! NumPy array supports different data types where the array module doesn't support this kind of mixing. After calling the print function we found the output where we can see the elements are in integers and strings.
To see the type of the `TopTenNP` type: 

{{< codeblock  "numpyExample.py">}}

print(type(TopTenNP))

{{< /codeblock >}}

```
Output: <class 'numpy.ndarray'>
```

**NumPy Array** is a powerful multi-dimensional array object. It can also be formed of rows and columns. 

Let's see some operations of NumPy Array:

{{< codeblock  "numpyOperationsExample.py">}}

#To create a random (rows*columns = 2 * 2) array with integer elements

array1 = np.arange(4, dtype = np.int_).reshape(2, 2)    

"""

Output:

[[0 1]
 [2 3]]

""" 	

#To create an array of 4-byte integer elements by assigning their values

array2 = np.array([[1, 2], [4, 5]], np.int32)    

"""

Output:

[[1 2]
 [4 5]]

""" 																	 

#To get addition of two arrays

np.add(array1, array2)

"""

Output:

array([[1, 3],
       [6, 8]])

"""

#To get subtraction of two arrays

np.subtract(array1, array2)

"""

Output:

array([[-1, -1],
       [-2, -2]])

"""

#To get multiplication of two arrays

"""

Output:

array([[ 0,  2],
       [ 8, 15]])

"""

#To get division from two arrays

np.divide(array1, array2)

"""

Output:

array([[0. , 0.5],
       [0.5, 0.6]])

"""

#To apply power operation on two arrays

np.power(array2, array1)

"""

Output:

array([[  1,   2],
       [ 16, 125]])

"""

np.power(array2, 2)   # array2 to the power (2) 

"""

Output:

array([[ 1,  4],
       [16, 25]], dtype=int32)

"""

#To get mod of two arrays

np.mod(array1, array2)

"""

Output:

array([[0, 1],
       [2, 3]])

"""

np.mod(array2, 2)   # array2 mod by 2

"""

Output:

array([[1, 0],
       [0, 1]], dtype=int32)

"""

{{< /codeblock >}}

### Revision: What is a List?

**A list** is a built-in data structure in Python that can store a sequence of objects. Like Array, for *N* length of **List** has elements indexed from 0 to *N*-1. 

A list is also ordered, mutable but doesn't need to be unique in Python. We can combine strings, integers, and objects, etc. different data types in the same list and it can have values appended, removed, or changed.

{{< codeblock  "listExample.py">}}

TopTenList = [10, 'Twenty', 30, 40, 50, 60, 'Seventy', 80, 'Ninty', 100]
print(TopTenList)

{{< /codeblock >}}

```
Output: [10, 'Twenty', 30, 40, 50, 60, 'Seventy', 80, 'Ninty', 100]
```

Here we don't need to import any module or packages to use a List in Python cause List is a built-in data structure in Python. We took a variable named ToptenList and assigned some elements in different data types. The list supports different data types like NumPy Array. In the output we can see the elements are showing in integers and strings as to how Python interpreter does this always for us! 

To see the type of the `TopTenList` : 

{{< codeblock  "listExample.py">}}

print(type(TopTenList))

{{< /codeblock >}}

```
output: <class 'list'>
```

Let's see some operations on `TopTenList`:

{{< codeblock  "ListOpeartionExample.py">}}

#Use `listname.append ` to add an element into the last index of a list.

TopTenList.append(110)     # [10, 'Twenty', 30, 40, 50, 60, 'Seventy', 80, 'Ninty', 100, 110]

#Use `listname.inser('index No.', 'element')` to add an element into a certain position of a list.

TopTenList.insert(0, 'Zero')    # ['Zero', 10, 'Twenty', 30, 40, 50, 60, 'Seventy', 80, 'Ninty', 100, 110]

#Use `listname.remove` to remove an element from a list

TopTenList.remove('Ninty')    # ['Zero', 10, 'Twenty', 30, 40, 50, 60, 'Seventy', 80, 100, 110]

#Use list.reverse() to reverse a list

list.reverse(TopTenList)    # [110, 100, 80, 'Seventy', 60, 50, 40, 30, 'Twenty', 10, 'Zero']

#To modify a fixed position of index of a list

TopTenList[2] = 'Ninty'    # [110, 100, 'Ninty', 'Seventy', 60, 50, 40, 30, 'Twenty', 10, 'Zero']

{{< /codeblock >}}

### Revision: What is a Tuple?

A tuple is almost as like as the list data type, except in two ways. First, tuples are typed with parentheses, ( values ), instead of square brackets, [ values ], another is that the Tuples cannot have their values modified, appended, or removed. We can convert the tuple into a list, change the list, and convert the list back into a tuple and that is the one way to modify a tuple.

{{< codeblock  "tupleExample.py">}}

TopTenTuple = ('10','20','Thirty',40, 50, 60, 'Seventy', 80, 'Ninty', 100)
print(TopTenTuple)

{{< /codeblock >}}

```
('10', '20', 'Thirty', 40, 50, 60, 'Seventy', 80, 'Ninty', 100)
```

As like List, here we don't need to import any module or packages to use a Tuple in Python cause Tuple is also a built-in data structure in Python. We took a variable named ToptenTuple and assigned some elements in different data types. 

To see the type of the `TopTenTuple` : 

{{< codeblock  "tupleExample.py">}}

print(type(TopTenTuple))

{{< /codeblock >}}

```
output: <class 'tuple'>
```

### So when and where we will use among these three types?

We know that It's a best practice to use the right data structure to write a good program. So now we will have a look at some practical uses of Arrays, Lists, and Tuples.

Among these three types, **Arrays** are great for numerical, arithmetic operations and can store data very compactly and are more efficient storing a **large** collection of similar **data types**. When we use the array module instead of the list, Python doesn't have to remember the data type details of each element. NumPy Arrays are widely used in the data science world to work with multidimensional arrays for their efficiency of handling of large datasets. On the other hand operations on **tuples** can be executed **faster** compared to operations on **lists**. But when we need to modify the values it's quite efficient to use List and Array as they are mutable than using a Tuple. To use different data types List can be most useful among these three although Tuple can contain elements from different data types  but for the immutable issue it's better to use a List than a Tuple.

In the next part of this topic, we will see more discussion about Array-based sequences in Python and their operations in more detail. Till then, have a good night to you all!     







Photo [Designed by pressfoto](http://www.freepik.com)

