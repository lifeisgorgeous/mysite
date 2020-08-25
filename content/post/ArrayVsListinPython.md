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

I started to explore the uses of the data structures in Python. Suddenly, a simple question stuck in my mind that can we use a list in replace of an array in Python. Then I started a little research from books and over the Internet and tried to tie up what I learn in this blog.  

**Note**: In Python, we write programs from an abstraction level, that’s why it’s also called high-level programming language that means Python is more human-readable code than machine-readable. To understand the core concept of an Array based sequences more in-depth, in the Part 2 of this blog we will discuss the concept of the low level array and dynamic array class in Python. I will try to write more relevant details of those concepts in the next part very soon! This blog may not be helpful for very beginners in programming. For whom it may concern, who knows Python or any other programming language or the basics of programming let’s deep dive into the similarities and differences between Array, List and Tupples using Python!

###  Revision: What is an Array?

An array is a data structure and a collection of elements of the same type. The elements are referenced by their index. For N elements index is started from 0 to N - 1. We can do append, remove and modify operations on an Array.

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

In the code snippets we can see that, we imported the NumPy package and named it np. Then we took a variable named ToptenNP and assigned some elements in different data types. Yes! NumPy array supports different data types where the array module doesn't support this kind of mixing. After calling the print function we found the output where we can the elements are in integers and strings.
To see the type of the `TopTenNP` type: 

{{< codeblock  "numpyExample.py">}}

print(type(TopTenNP))

{{< /codeblock >}}

```
Output: <class 'numpy.ndarray'>
```



### Revision: What is a List?

**A list** is a built-in data structure in Python that can store a sequence of objects. Like Array, for *N* length of **List** has elements indexed from 0 to *N*-1. 

A list is also ordered, mutable but doesn't need to be unique in Python. We can combine strings, integers, and objects, etc. different data types in the same list and it can have values appended, removed, or changed..

{{< codeblock  "listExample.py">}}

TopTenList = [10, 'Twenty', 30, 40, 50, 60,'Seventy',80,'Ninty',100]
print(TopTenList)

{{< /codeblock >}}

```
Output: [10, 'Twenty', 30, 40, 50, 60, 'Seventy', 80, 'Ninty', 100]
```

{{< codeblock  "listExample.py">}}

Here we don't need to import any module or packages to use a List in Python cause List is an buit-in data structure in Python. We took a variable named ToptenList and assigned some elements in different data types.  List supports different data types as like as NumPy Arrays. In the output we can the elements are showing in integers and strings as how Python interpret does this always for use! 

To see the type of the `TopTenList` : 

print(type(TopTenList))

{{< /codeblock >}}

```
output: <class 'list'>
```



### Revision: What is a Tuple?

A tuple is almost as like as the list data type, except in two ways. First, tuples are typed with parentheses, ( values ) , instead of square brackets, [ values ] another is Tuples cannot have their values modified, appended, or removed. 







Photo [Designed by pressfoto](http://www.freepik.com)

