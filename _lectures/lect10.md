---
annotatedpdfurl: /lectures/CS16_Lecture10_ann.pdf
annotatedready: true
desc: The good, bad and ugly about pointers, C++ Memory Model, Dynamic memory allocation (Heap), Heap vs Stack
lecture_date: 2020-05-04
num: Lecture 10
slides: /lectures/CS16_Lecture11.pdf
ready: true

---

# Lecture Video

<https://youtu.be/rYPnalyY-Co>

I went the full time today, so I'll make it up to you with a shorter video on Wednesday!

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
