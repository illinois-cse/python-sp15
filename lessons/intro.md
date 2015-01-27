## **Introduction**

[This](https://www.desmos.com/calculator) is like an online version of your graphing calculator, and you can do some cool math calculations with it.

But what have you actually been doing here? Programming!

We use programming in this kind of a small way every day. Why? It saves us a lot of time. 

![Comic](http://www.jeffpalm.com/fox/fox.jpg)

Great! I get it. Programming is useful. But ...

### Why Python?

Let’s look at the ABCs of programming, a.k.a. the `Hello World` program.

If you were to use *C*, you’d be punching in these few lines here:

    #include <stdio.h>
    
    int main(int argc, char *argv[]) {
        printf("Hello World");
    }

*Fortran* would be less intuitive and more ludicrous and make you type:

    program hello
        print *, "Hello World!"
    end program hello

While, with *Python*, you just have to say :

    print "Hello World!"

We can clearly see, Python reduces a lot of human time. Apart from doing that, it is:
-   Free
-   Widely used
-   Great for visualization

Now that we have (hopefully) convinced ourselves that studying Python is not a waste of time, let’s get started!

## **Built-in types and variables**

*Numbers*

Python can easily substitute your calculator to help do basic math!

**Examples**

-   `17+4`

-   `10*6`

-   `9-9`

-   `2**5`

-   `5%2`

*Strings*

`"Go Illini"`

Can also be written, `'Go Illini'`

Python makes string concatenation (connection) trivial:

`"Go" + "Illini"`

*Variables*

Variables form the backbone of any program. 

    x=3
    x="It is too early in the morning"

The point here to note is that `x` does not need a pre-defined data type, as in other programming languages like C or C++.  Python is smart enough to figure out *what* `x` is and adjust accordingly (but this slows it down a bit which is why many languages do not do this).

Note the difference between a variable and a string.  I can have a variable `new="new"`.

### **Exercise 1**

1. What is the difference between `17/4` and `17/4.0`?

2. Print `"It's too early in the morning"`

3. Using the numbers 4 and 6 the math operations: +, -, *, / print the number 8.

4. If `x="abcde"`, then what are `x[0]`, x[-1]`, and `x[1:]`?


**Other Built-in Types**

*Boolean*

Can either be `True` or `False`

    x=True
    print x
    x=False
    print x

Reverse it:  `print not x`

Question: Can you print `True` without assigning it to `x`? _i.e._, without using any other operators? 

**Aside: Comparison Operators**

    6 > 4 #True
    6 < 4 #False

Question:
    a=3
    b=3.0
What is `a==b`?  Why?

*Lists*

From strings and numbers, we are now moving to more compound datatypes. 

Lists are collections of variables.  In Python, lists are written as comma separated values within square brackets.

    myfirstlist= [1,2,3,4]

Now we can manipulate all of these values as a unit.  Where might you use this capability?

Some properties of lists:

1. Heterogenous:
    myfirstlist=[1,2,"apple",3]

2. Can be sliced and indexed
    myfirstlist[0] #1
    myfirstlist[-1] #3
    myfirstlist[-3:] #[2,’apple’,3]

3. Lists are mutable
    myfirstlist[0]="orange"

### **Exercise 2**
Try the following:

    myfirstlist.append(5)
    myfirstlist.insert(1,5)
    myfirstlist.sort()
    myfirstlist.reverse()
    myfirstlist.count(5)
    myfirstlist.remove(5)

Lists are associated with built-in ‘methods’ which is what you saw in the above exercise.

*Tuples*
A tuple consists of a number of values separated by commas, for instance:

    myfirsttuple=(1,2,"apple",3)

They are quite similar to lists in most ways.  But try,
    myfirsttuple[0]="orange"

So, tuples are _____________?

*Dictionaries*

A dictionary is a set of `key:value` pairs---in other words, an index to look up a data point.  They are quite useful in advanced programming as we will see later on.

**Example:**

    myfirstdict = {‘a’:1, ‘b’:2, ‘c’:3}
    'a' in myfirstdict #True

## **Conditionals and Loops**

So we now know variables, built in data types and comparison operators. So what do we do with all of this? We need to structure this 
into a program for which we need to understand conditionals and loops.To write a structured program, we need to be writing a Python
script.

### **Writing a Python script**

All this was done using the interactive Python interface.  Now we will move on to writing Python scripts, or persistent text files which can be executed again and again.

To write a Python script, we need an editor

-   Open the editor and write:
    `print "This is a Python Script"`

-   Save as pythonscript.py

-   Run it from the command line: `python pythonscript.py`

### **Conditionals**

What are conditional statements?

    if (6>4):
        print “True”
    else:
        print “Not true”

### **Exercise 3**

-   Write a Python script to check if a number is even or odd or zero.

### **Loops**

Why do we need loops?

There are many instances where you need to run the same lines of code multiple times.

**Example:  Factorial**

    n!=n*(n-1)*(n-2)…..*3*2*1
    5!=5*4*3*2*1

Without loops, we would need to write the same multiplication code 5 times.

### **Exercise 4**

-   Write a Python script to check if a Number is prime or not.  Use the definition of a prime number as one with only two factors---one and the number itself.

**Looping through lists**

Accessing and using lists is intrinsically linked to loops. For instance,

    mylist=[1,2,3,4]
    for i in range(0,4):
        print i, mylist[i]

## **Functions and Libraries**

Python has quite a few built in standard libraries, and the extended library ecosystem is one of the major advantages to using Python today.  To name a few:
-   `math`
-   `scipy`
-   `numpy`

Each of these libraries have a number of modules or functions.

**Example: Using `math.sqrt` to find the square root**

    import math
    print math.sqrt(9)

    from math import sort
    print sqrt(9)

    import math as mt
    print mt.sqrt(9)

Apart from the standard functions, we can declare user defined functions too.

The structure of a new function is: 

    def function_name(input arguments):
        function defintion
        return output

**Example:**

    def areaSquare(a):
        return a**2

### **Exercise 5**

Modify the previous exercise(to check for a prime number), to a function.

Each Python file can in turn be used as a library, where you import the Python file and function you need.

    import area
    print area.areaSquare(2)

### **Exercise 6: the big one**

Using the file which stores the Prime Number function, create a new Python script, where you declare a list of numbers (`x=1, 2 .. 100`).
and loop through the numbers in the list to count the number of prime numbers.


