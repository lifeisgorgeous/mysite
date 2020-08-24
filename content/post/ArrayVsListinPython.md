---
title: "Data Structure Using Python: Array Vs List"
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
- Python
thumbnailImage: https://res.cloudinary.com/ddlohuyww/image/upload/v1598290385/images/18705_iimcyw.png
thumbnailImagePosition: "top"
thumbnailImage: https://res.cloudinary.com/ddlohuyww/image/upload/v1598290385/images/18705_iimcyw.png
coverImage: https://res.cloudinary.com/ddlohuyww/image/upload/v1598290385/images/18705_iimcyw.png
metaAlignment: center
coverCaption: "Photo by pressfoto"
---

<!--more-->

### Data Structure Using Python: Array Vs List

I started to explore the uses of the data structure in Python. Suddenly, a simple question stuck in my mind that can we use a list in replace of an array in Python. Then I started a little research from books and over the Internet and tried to tie up what I learn in this blog.  

*Prerequisites*: 

In Python, we write programs from an abstraction level, that’s why it’s also called high-level programming language that means Python is more human-readable code than machine-readable. To understand the core concept of an Array more in-depth you can study Array using C or C++ programming language where we have to use data type and can understand memory representation more clearly. I will try to write relevant to that topic in the future. This blog may not be helpful for very beginners in programming. For whom it may concern, who knows python or any other programming language or the basics of programming let’s deep dive into the similarities and differences between Array and List using python!

###  Revision: What is Array?

An array is a data structure and a collection of elements of the same type. The elements are referenced by their index. For N elements index is started from 0 to N - 1.

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



### Revision: What is List?

**A list** is a built-in data structure in Python that can store a sequence of objects. Like Array, for *N* length of **List** has elements indexed from 0 to *N*-1. 

A list is also ordered, mutable but doesn't need to be unique in Python. We can combine strings, integers, and objects, etc. different data types in the same list.

{{< codeblock  "listExample.py">}}

TopTenList = [10, 'Twenty', 30, 40, 50, 60,'Seventy',80,'Ninty',100]
print(TopTenList)

{{< /codeblock >}}

```
Output: [10, 'Twenty', 30, 40, 50, 60, 'Seventy', 80, 'Ninty', 100]
```

{{< codeblock  "listExample.py">}}

print(type(TopTenList))

{{< /codeblock >}}

```
output: <class 'list'>
```

Photo [Designed by pressfoto](http://www.freepik.com)

