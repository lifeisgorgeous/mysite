---
title: "Data Structures Using Python: Array Based-Sequences [Part -1]"
description: "Array Vs List Vs Tupple"
date: 2020-08-24T23:22:47+06:00
categories:
- Data Structure
tags:
- Python
- Programming
keywords:
- tech
- Array
- List
- Tuple
- Python
thumbnailImage: https://res.cloudinary.com/ddlohuyww/image/upload/v1598290385/images/18705_iimcyw.png
thumbnailImagePosition: "top"
thumbnailImage: https://res.cloudinary.com/ddlohuyww/image/upload/v1598290385/images/18705_iimcyw.png
coverImage: https://res.cloudinary.com/ddlohuyww/image/upload/v1598290385/images/18705_iimcyw.png
metaAlignment: center
coverCaption: "Photo by pressfoto"
---

<!--more-->

### Array V/s List V/s Tupple 

I started to explore the uses of the data structures more in-depth in Python. Suddenly, a question stuck in my mind that can we use a list in replace of an array in Python. Then I started a little research from books and over the Internet and tried to tie up what I learn in this blog.

**Note**: In Python, we write programs from an abstraction level, that’s why it’s also called high-level programming language that means Python is more human-readable code than machine-readable. To understand the core concept of an Array-based sequence more in-depth, in Part 2 of this blog we will discuss the concept of the low-level array and dynamic array class in Python. I will try to write more relevant details of those concepts in the next part very soon! This blog may not be helpful for very beginners in programming. For whom it may concern, who knows Python or any other programming language or the basics of programming let’s deep dive into the similarities and differences between Array, List, and Tuple using Python!

###  Revision: What is an Array?

An array is a data structure and a collection of elements of the same type. The elements are referenced by their index. For N elements index is started from 0 to N - 1. 

We can do append, remove, and modify operations on an Array.

In Python, arrays are ordered, mutable, and can be stored as non-unique items. 

There are two ways to use an Array in Python: 

i) Importing by Array module:

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

ii) Importing by NumPy Packages:

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

We know It's very important to use the right data structure to write a good program. So now we will have a look at some useful uses of Array, List, Tuple.

Among these types, **Arrays** are great for numerical, arithmetic operations and can store data very compactly and are more efficient storing **large** amounts of **data**. On the other hand operations on **tuples** can be executed **faster** compared to operations on **lists**. But when we need to modify the values it's quite efficient to use List and Array as they are mutable than using a tuple. To use different data types List can be most useful among these three although Tuple can contain elements from different data types for the immutable issue it's better to use List than Tuple.

In the next part of this topic, we will see more discussion about Array-based sequences in Python and their operations in more detail. Till then have a good night to you all!     







Photo [Designed by pressfoto](http://www.freepik.com)

