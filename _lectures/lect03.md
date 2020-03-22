---
annotatedpdfurl: /lectures/CS16_Lecture3_ann.pdf
annotatedready: true
desc: Loops (for, while, do-while), doubles, functions
lecture_date: 2020-04-06
num: Lecture 3
slides: /lectures/CS16_Lecture3.pdf
ready: false

---

<!--
# Lecture videos

You should change the quality to the highest setting. And I'm sorry that I say "uh" a lot—at least you can watch at twice the speed and get it over with!

- Precedence, assigning using constructors, `cerr` (watch this first): <https://www.youtube.com/watch?v=J5mCrJ3yUlg>
- Main lecture: <https://www.youtube.com/watch?v=06yplj26938>
-->

# Code from lecture

<https://github.com/ucsb-cs16-m19/code-from-class/tree/master/07-02>

# Topics

## Working with doubles
* Evaluating expressions with mixed numeric types
* Typecasting int to double 
* Formatted output with doubles:

Comment each line of code. What is the output of the code?
```
int i = 10;
double j = 1/static_cast<double>(i);
cout.setf(ios::fixed);
cout.setf(ios::showpoint);
cout.precision(3);
cout<<j<<endl;
```
## Practice with single for loops
* Summing a series: 

**Exercise: Write a program that takes a parameter n as a command line arguments and computes the following:**

```
1 + 1/2 + 1/3 + ....+ 1/n
```
where n is the number of terms in the series. Sample run of the program is below:

```
$./sumSeries 2
Sum of the first 2 terms is: 1.500
```
## Nested Loops

ASCII Art with nested loops

**Math Puzzle**

One of the powers of computing is being able to do a brute-force search for a solution to a problem. Trial and error works just fine for some problems. In fact, computers can be especially good at such problems. Consider this:

Horses cost $10, pigs cost $3, and rabbits are only $0.50. A farmer buys 100 animals for $100, How many of each animal did he buy?  

Write a program to do this.

## Precedence

