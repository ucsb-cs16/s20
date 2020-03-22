---
annotatedpdfurl: /lectures/CS16_Lecture10_ann.pdf
annotatedready: true
desc: The good, bad and ugly about pointers, C++ Memory Model, Dynamic memory allocation
  (Heap), Heap vs Stack
lecture_date: 2019-08-01
num: Lecture 10
slides: /lectures/CS16_Lecture11.pdf
ready: true

---

# Code from lecture

<https://github.com/ucsb-cs16-m19/code-from-class/tree/master/08-01>

# Stuff I wrote on the "whiteboard"

Go here and click on the appropriate date:
<https://1drv.ms/o/s!AlgIeD1urAgmgQU7loNfb3-LYrma>

# Topics

The good:

* Pointers allow arrays to be passed to functions efficiently
* Pointers allow arrays of large structs to be traversed effiently

The bad:

* Pointers can only point to one type of data (not generic)
* They don't automatically point - need to do some work

The ugly

* Bugs in code that involves pointers can cause your program to irrecoverably crash (Segmentation fault)
* Examples: dereferencing a null pointer, out of bound array access, dereferncing a pointer that has junk value.

## C++ Memory model
* Barebones model of memory: value vs address
* Scope: local vs. global
* Layout of compiled C++ program in memory: text, global data , heap and stack


* A first look at dynamic memory allocation
* The hows and whys of creating data on the stack vs. heap
