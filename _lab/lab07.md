---
assigned: 2020-05-18 00:00
desc: Linked lists
due: 2020-05-24 23:59
layout: lab
num: lab07
ready: true

---


# Goals of this lab

The goal of this lab is get more practice with iterating through linked lists and solving problems. Continue to practice code tracing to reason about your code. We request that you DO NOT ask the staff to debug your code, but instead ask them to guide you in the debugging process.

# Step by Step Instructions: PLEASE READ CAREFULLY!

## Step 1: Getting Started

1. Decide if you are working alone, or working in a pair.

2. Choose who will be the first driver and who will start as navigator, and then remember to switch (at least once) during the lab.

3. Go to github and create a git repo for this lab following the naming convention specified in previous labs. If you are working with a partner only one of you needs to create the repo.

4. If you are working with a partner and you are the one who created the github repo, add your partner as a collborator on the repo

5. Decide on initial navigator and driver.

6. Driver, log on to your CSIL account.

7. Open a terminal window and log into the correct machine.

8. Change into your CS 16 directory

Note: Remember to push your work to github at the end of EVERY work session. That way, both partners always have access to the latest version of the code even if the code is being developed on one partner's CoE account.



## Step 2: Obtaining the starter code


* Navigate to your cs16 directory and clone the git repository you created
```
git clone git@github.com:ucsb-cs16-s20-nichols/lab07_alily_jgaucho.git
```
* cd into this new directory
```
cd lab07_alily_jgaucho
```

* **If you're on your local machine**, please follow the instructions from lab01 to download the starter code for every lab. Then you can copy the lab07 starter code (in the lab07 folder) into the folder that your `git` command just created.

* **If you are using CSIL**, Copy the starter code by using the `cp` command below.

* Copy the starter code by typing the following command:

```
cp /cs/student/lawtonnichols/cs16/labs/lab07/* ./
```

Typing the list (ls) command should show you the following files in your current directory

```
[lawtonnichols@csil-03 lab07-startercode]$ ls
linkedListFuncs.cpp  Makefile                 tddFuncs.cpp
linkedListFuncs.h    moreLinkedListFuncs.cpp  tddFuncs.h
linkedList.h         moreLinkedListFuncs.h
llTests.cpp          README.md
[lawtonnichols@csil-03 lab07-startercode]$
```


## Step 3: Reviewing the files and what your tasks are

Here is a list of your tasks for this lab:

### Step 3a: Familiarize yourself with the big picture

Type "make tests" and you will see some tests pass, but some fail.

You are finished when all the tests pass. We have implemented a few function that involve linked lists in `linkedListFuncs.cpp`. There is only one file you need to edit this week:

<code>moreLinkedListFuncs.cpp</code> contains more functions that deal with linked lists.  


### Step 3b: Work on the linked list functions

Working on the linked list functions below is one of the most important things you can do to prepare for the final exam.

There are 7 functions you will need to write for this lab:

* <code>addIntToEndOfList</code>
* <code>addIntToStartOfList</code>
* <code>pointerToMax</code>
* <code>pointerToMin</code>
* <code>largestValue</code>
* <code>smallestValue</code>
* <code>sum</code>


Each one has a set of tests which can be found under its corresponding heading when you type <code>make tests</code>. For example, the addIntToEndOfList tests look like this to start: 

```
./llTests 1
--------------ADD_INT_TO_END_OF_LIST--------------
PASSED: linkedListToString(list)
   FAILED: linkedListToString(list)
     Expected: [42]->[57]->[61]->[12]->null Actual: [42]->[57]->[61]->null
   FAILED: linkedListToString(list)
     Expected: [42]->[57]->[61]->[12]->[-17]->null Actual: [42]->[57]->[61]->null
PASSED: linkedListToString(empty)
   FAILED: linkedListToString(empty)
     Expected: [0]->null Actual: null
   FAILED: linkedListToString(empty)
     Expected: [0]->[19]->null Actual: null

```

You should replace each function stub with the correct code for the function until all of the tests for each one pass. It is recommended that you work on the functions one at a time in the order that they are presented above. That is, get all the tests to pass for addIntToStartOfList then addIntToEndOfList and so on. When all the tests pass, move on to the next step. 

## Step 4: Checking your work before submitting

When you are finished, you should be able to type  <code>make clean</code> and then <code>make tests</code> and see the following output:


```
-bash-4.2$ make clean
/bin/rm -f llTests *.o
-bash-4.2$ make tests
g++ -Wall -Wno-uninitialized   -c -o llTests.o llTests.cpp
g++ -Wall -Wno-uninitialized   -c -o linkedListFuncs.o linkedListFuncs.cpp
g++ -Wall -Wno-uninitialized   -c -o moreLinkedListFuncs.o moreLinkedListFuncs.cpp
g++ -Wall -Wno-uninitialized   -c -o tddFuncs.o tddFuncs.cpp
g++ -Wall -Wno-uninitialized  llTests.o linkedListFuncs.o moreLinkedListFuncs.o tddFuncs.o -o llTests
./llTests 1
--------------ADD_INT_TO_END_OF_LIST--------------
PASSED: linkedListToString(list)
PASSED: linkedListToString(list)
PASSED: linkedListToString(list)
PASSED: linkedListToString(empty)
PASSED: linkedListToString(empty)
PASSED: linkedListToString(empty)
./llTests 2
--------------ADD_INT_TO_START_OF_LIST--------------
PASSED: linkedListToString(list)
PASSED: linkedListToString(list)
PASSED: linkedListToString(list)
PASSED: linkedListToString(empty)
PASSED: linkedListToString(empty)
PASSED: linkedListToString(empty)
./llTests 3
--------------POINTER_TO_MAX--------------
PASSED: pointerToMax(list1)
PASSED: pointerToMax(list1)
PASSED: pointerToMax(list1)->data
PASSED: pointerToMax(list1)->next->data
PASSED: pointerToMax(list2)
PASSED: pointerToMax(list2)
PASSED: pointerToMax(list2)->data
PASSED: pointerToMax(list3)
PASSED: pointerToMax(list3)
PASSED: pointerToMax(list3)->data
PASSED: pointerToMax(list4)
PASSED: pointerToMax(list4)
PASSED: pointerToMax(list4)->data
PASSED: pointerToMax(list4)->next->data
./llTests 4
--------------POINTER_TO_MIN--------------
PASSED: pointerToMin(list1)
PASSED: pointerToMin(list1)
PASSED: pointerToMin(list1)->data
PASSED: pointerToMin(list1)->next->data
PASSED: pointerToMin(list2)
PASSED: pointerToMin(list2)
PASSED: pointerToMin(list2)->data
PASSED: pointerToMin(list3)
PASSED: pointerToMin(list3)
PASSED: pointerToMin(list3)->data
PASSED: pointerToMin(list4)
PASSED: pointerToMin(list4)
PASSED: pointerToMin(list4)->data
PASSED: pointerToMin(list4)->next->data
./llTests 5
--------------LARGEST_VALUE--------------
PASSED: largestValue(list1)
PASSED: largestValue(list2)
PASSED: largestValue(list3)
PASSED: largestValue(list4)
./llTests 6
--------------SMALLEST_VALUE--------------
PASSED: smallestValue(list1)
PASSED: smallestValue(list2)
PASSED: smallestValue(list3)
PASSED: smallestValue(list4)
./llTests 7
--------------SUM--------------
PASSED: sum(list1)
PASSED: sum(list2)
PASSED: sum(list3)
PASSED: sum(list4)

-bash-4.2$
```

At that point, you are ready to try submitting on gradescope.


## Step 5: Submitting via gradescope

Submit the moreLinkedListFuncs.cpp file on gradescope. Make sure to add your partner as a collaborator if you had one.

## Gradescope automatic points

<table border="1">
<tr><th>Test Name</th><th>Value</th></tr>
<tr><td><p style="color:green;margin:0;padding:0;">addIntToEndOfList</p></td><td>(10 pts)</td></tr>
<tr><td><p style="color:green;margin:0;padding:0;">addIntToStartOfList</p></td><td>(10 pts)</td></tr>
<tr><td><p style="color:green;margin:0;padding:0;">pointerToMax</p></td><td>(10 pts)</td></tr>
<tr><td><p style="color:green;margin:0;padding:0;">pointerToMin</p></td><td>(10 pts)</td></tr>
<tr><td><p style="color:green;margin:0;padding:0;">largestValue</p></td><td>(10 pts)</td></tr>
<tr><td><p style="color:green;margin:0;padding:0;">smallestValue</p></td><td>(10 pts)</td></tr>
<tr><td><p style="color:green;margin:0;padding:0;">sum</p></td><td>(10 pts)</td></tr>
</table>
