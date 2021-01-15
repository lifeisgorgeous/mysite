---
Draft: False
title: "Learn Bash Script"
date: 2021-01-03T17:52:50+06:00
categories:
- Bash
-  
tags:
- bash
- 
keywords:
- 
#thumbnailImage: //example.com/image.jpg
---

## Learn Bash Script

------

**Prerequisites:**  Experience ( At least Beginner Level) with Linux or OS X command line, fundamentals of programming

**Main Focus:** Multi line scripts.

**Prior Setup:** 

- nano/vim/emacs or sublimeText/TextWrangler/TextMate/gedit etc.
- Linux machine or virtual machine or Mac OS X ternminal

**For the windows user:**

- Set a local linux virtual machine.
- Set PuTTy to connect to a linux machine.
- A ports of Bash for windows also exists.
- Look into bacth scripts to script for windwos.

In this blog we will use nano editor on Ubuntu 20.04 terminal.

 To check *bash* version type from terminal:

```t
echo $BASH_VERSION
```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712404/images/img/01_batz96.png)

### What is BASH?

- Bourne Again Shell
- A popular interactive command line interpreter.

### History by Year:

- 1971: Thompson Shell (first UNIX shell)

- 1975: Mashey Shell

- 1977: Bourne Shell (sh)

  some features from ALGOL

- 1978: C Shell (csh) - more similiar to C

- 1989: Bourne Again Shell (Bash) - Released by Brian Fox for GNU Project (gnu.org), maintained by Chet Ramey 

```bash
pwd # Current working directory
ls # List all the files and directory of current working driectory
ls directory_name # List all the files and directory of specific driectory
ls -l directory_name # List all the details informations of the specific driectory
```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712405/images/img/02_rhktss.png)

```bash
man ls # Gives manual pages of ls
q # Enter q to quit from manual pages
```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712404/images/img/03_pedn7y.png)

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712404/images/img/04_pkfviv.png)

```bash
mkdir directory_name # To create a new directory
rmdir directory_name # To remove a directory

```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712404/images/img/05_vqoph4.png)

```bash
cd directory_name # To change the current directory to a specific directory
touch filename # To create a new file
rm filename # To delete a file
```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712404/images/img/06_ey3gok.png)

```bash
nano apple.txt # To edit a text file using nano editor
```

**nano Editor:**

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712404/images/img/07_oj6rqr.png)

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712404/images/img/08_ewnlmc.png)

```bash
cat filename1 # To concatent strings in a sinle text file
cat filename1 filename2 # To concatent all the strings in bewtwen two files
```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712403/images/img/09_iw93jd.png)

```bash
more largetextfilename # To read a large text files

```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712403/images/img/10_n3tgga.png)

```bash
head largetextfilename # To read the first few lines of a large text file
tail largetextfilname # To read the last few lines of a large text file
```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712403/images/img/11_xmbu7p.png)

```bash
touch file_{1..1000} # To create 1000 files with filename 'file_1' to 'file_1000'
```

Uperlimit of this range varies by platform to platform. On OS X 14340 and on linux this is much higher than that.

```bash
touch {apple, banana, mangoe}_{01..100}{w..d} # To create a file using variety of words, letter and numbers
```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712403/images/img/13_ez5acy.png)

```bash
ls -1 | wc -l # To count the created files
```

![](https://res.cloudinary.com/ddlohuyww/image/upload/v1610712402/images/img/14_tydb68.png)

To be continued ...