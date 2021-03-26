---
title: "Variables"
teaching: 0
exercises: 0
questions:
- "What is a variable?"
- "What is a type?"
objectives:
- "Use variables to store values and do calculations"
keybpoints:
- "What is a variable?"
- "What types of variables are available in Java?"
---

In computer programming a variable is a symbolic name for a specific area in the computer's memory where a value is stored. In Java we have to define a variable before we can use it and when we define it, we have to specify the type of information we will be storing in the variable.

In Java we have the following types available which we can use to define what information will be stored in a variable:

- ```byte:``` stores whole numbers from -128 to 127
- ```short:``` stores whole numbers from -32768 to 32767
- ```int:``` stores whole numbers from -2<sup>31</sup> to 2<sup>31</sup>-1.
- ```long``` stores whole numbers from -2<sup>63</sup> to 2<sup>63</sup>-1.
- ```float:``` stores fractional numbers with 6 to 7 decimal digits
- ```double:``` stores fractional numbers with 15 decimal digits
- ```boolean:``` stores true or false
- ```char:``` stores a single character from UNICODE

In addition to these types, Java provides special support for strings with the ```String``` type. Note the capitalisation of the ```String``` type. We'll just mention the reason for the capitalisation but we won't discuss it in more detail. String is a class whereas the other types we mentioned are known as primitives. 

Each of these types use a different amount of memory.

Create a new repl and call it ```03.Variables```. Enter the following code and compile and run it:

```java
1  // Define the class
2  class Main {
3   // Define the main method
4   public static void main(String[] args) {
5     // Define variables and initialise them with values;
6     String stringVariable = "Print ten plus ten: ";
7     int integerValue = 10;
8     // You can also define a variable without initialising it;
9     int total;
10    System.out.println(stringVariable);
11    System.out.println(stringVariable + integerValue + 10);
12    System.out.println(stringVariable + integerValue + integerValue);
13    System.out.println(stringVariable + (integerValue + integerValue));
14    // Do some multiplication and store the value in the variable total
15    // Storing a value in a variable is called assingment
16    total = integerValue * integerValue * 10;
17    System.out.println("Print the value of total: " + total);
18  }
19}

```
```bash
Print ten plus ten: 
Print ten plus ten: 1010
Print ten plus ten: 1010
Print ten plus ten: 20
Print the value of total: 1000
```

Let’s look at the program line by line:
- Note: By convention variable names start with lower-case.

1. The first line is just a comment
1. Define the beginning of a class named Main
1. Another comment
1. Declaring the main method (the front door to the program)
1. Yet another comment
1. ```String``` specifies the type of value that will be stored in the variable called ```stringVariable```. The ```=``` is an ***assignment operator***. The variable ```stringVariable``` will be ***assigned*** the value specified to the right of the ```=```, which in this case is ```Print ten plus ten: ```
1. ```int``` specifies the type of value that will be stored in ```integerValue```. The variable ```integerValue``` will be ***assigned*** the value specified to the right of the ```=```, which in this case is 10.
1. Another comment
1. On this line we declare yet another integer, called ```total```, using the ```int``` ***keyword*** but we don't assign a value to the variable.
1. Print some information to the console.
1. Print some information to the console.
1. Print some information to the console.
1. Print some information to the console.
1. Another comment
1. ... and yet another comment.
1. The variable ```total``` is assigned the value of the calculation ```integerValue * integerValue * 10```
1. Print the value of the variable ```total``` to the console.
1. Curly brace to close the ```main``` method.
1. Curly brace to close the class called ```Main```.


> ## Challenge
>
> Before leaving you to experiment with what you have learnt so far we are going to mention a couple more things to make it more interesting. 
> - **Operators**: Operators are characters that are used to perform actions on values.
> - Operators have **precedence**. That means that some operators have higher precedence than others. Operators with higher precedence are evaluated before operators with lower precedance. Operators on the same level of precedence are evaluated from left to right. Below is a table of operators. 
{: .challenge}

Here are a few of the operators:

|Operator|Function|Example|
|---|---|---|
|+|Addition|10 + 10, variable1 + variable2|
|-|Subtraction|10 - 5, variable1 - variable2|
|*|Multiplication|15 * 2, variable1 * variable2|
|%|Modulus|10 % 3, variable1 % variable2|
|/|Division|10 / 2|
|=|Assignment|total = variable1 + 10|





{% include links.md %}
