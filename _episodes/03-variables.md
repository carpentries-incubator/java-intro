---
title: "Variables and Types"
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

1. The first line is just a comment.
1. Define the beginning of a class named Main.
1. Another comment.
1. Declaring the main method (the front door to the program).
1. Yet another comment.
1. ```String``` specifies the type of value that will be stored in the variable called ```stringVariable```. The ```=``` is an ***assignment operator***. The variable ```stringVariable``` will be ***assigned*** the value specified to the right of the ```=```, which in this case is ```Print ten plus ten: ```.
1. ```int``` specifies the type of value that will be stored in ```integerValue```. The variable ```integerValue``` will be ***assigned*** the value specified to the right of the ```=```, which in this case is 10.
1. Another comment.
1. On this line we declare yet another integer, called ```total```, using the ```int``` ***keyword*** but we don't assign a value to the variable.
1. Print the content of the variable ```stringVariable``` to the console. 
1. Convert the number 10 and the integer value stored in ```integerValue``` to strings and then concatenate them to the string value stored in ```stringValue```. Print the final string to the console.
1. Convert the integer value stored in ```integerValue``` to  a string and then concatenate that twice to the string value stored in ```stringValue```. Print the final string to the console.
1. Add the integer value stored in ```integerValue``` to itself, convert the result to a string and then concatenate that to the string stored in ```stringAviable```. Print the final string to the console.
1. Another comment
1. ... and yet another comment.
1. The variable ```total``` is assigned the value of the calculation ```integerValue * integerValue * 10```
1. Convert the integer value stored in ```total``` to a string and concatenate it to the string ```Print the value of total:```. Print the final string to the console.
1. Curly brace to close the ```main``` method.
1. Curly brace to close the class called ```Main```.

## Operators

Before leaving you to experiment with what you have learnt so far we are going to mention a couple more things to make it more interesting. 
- **Operators**: Operators are characters that are used to perform actions on values.
- Operators have **precedence**. That means that some operators have higher precedence than others. Operators with higher precedence are evaluated before operators with lower precedance. Operators on the same level of precedence are evaluated from left to right. Below is a table of operators. The subheadings in the table groups the operators with the same precedence together. The groups are listed according to the precedence order. The closer to the top of the table a group appears, the higher its precedence. 

|Operator|Description|Example|
|---|---|---|
|**Postfix**|
|++ (Increment)|Increases the value of operand by 1.|B++ gives 21|
|-- (Decrement)|Decreases the value of operand by 1.|B-- gives 19|
|**Multiplicative**|
|* (Multiplication)|Multiplies values on either side of the operator.|A * B will give 200|
|/ (Division)|Divides left-hand operand by right-hand operand.|B / A will give 2|
|% (Modulus)|Divides left-hand operand by right-hand operand and returns remainder.|B % A will give 0|
|**Additive**|
|+ (Addition)|Adds values on either side of the operator.|A + B will give 30|
|- (Subtraction)|Subtracts right-hand operand from left-hand operand.|A - B will give -10|
|**Assignment**|
|= (Simple assignment operator)|Assigns values from right side operands to left side operand.|C = A + B will assign value of A + B into C|

> ## Challenge
>
> Take the next few minutes and see if you can write some code to do the calculations below.
> 1. Converting fahrenheit to celsius. The formula used for this is: ((fahrenheit - 32) * (5/9))
> 1. Converting celsius to fahrenheit. The formula used for this is: ((celsius * 9/5) + 32)
> 1. Converting celsius to kelvin: The formula used for this is: (celsius + 273.15)
> 1. Converting fahrenheit to kelvin: Can you work this one out yourself by using what you have already done?
>
> Steps:
> 
> - make four additional methods in Main; one for each of the calculations that a convert a value into another value. Go ahead and use the existing one as a skeleton (copy-paste) to be modified if you want.
> 
> Hints:
> 
> - your methods can `return` the converted value.
> - if methods with the `void` keyword terminates in a void, what might other variable types as method keywords enable the methods to do?
> - append `f` for float to 273.15 or java won't compute.
> 
> Suggestions:
> 
> - add more `System.out.println()` statements to explain the conversion by calling your methods with values of your choosing.
{: .challenge}
> - make one method and the accompanying printed explanation until you have made all four calculations.

> ## Solution
> ```java 
> class Main {
>   public static void main(String[] args) {
>     System.out.println("Calculate to convert!");
>     System.out.println(50 + " degrees Fahrenheit is " + fahrenheitToCelcius(50) + " degrees Celcius");
>     System.out.println(20 + " degrees Celcius is " + celciusToFahrenheit(20) + " degrees Fahrenheit");
>     System.out.println(10 + " degrees Celcius is " + celciusToKelvin(10) + " degrees Kelvin");
>     System.out.println(500 + " degrees Fahrenheit is " + fahrenheitToKelvin(500) + " degrees Kelvin");
>     System.out.println(0 + " degrees Fahrenheit is " + fahrenheitToKelvin(0) + " degrees Kelvin");
>   }
> 
>   public static float fahrenheitToCelcius(float fahrenheit) {
>     float celcius = (fahrenheit - 32) * 5 / 9;
>     return celcius;
>   }
> 
>   public static float celciusToFahrenheit(float celcius) {
>     float fahrenheit = (celcius * 9 / 5) + 32;
>     return fahrenheit;
>   }
> 
>   public static float celciusToKelvin(float celcius) {
>     float kelvin = celcius + 273.15f;
>     return kelvin;
>   }
> 
>   public static float fahrenheitToKelvin(float fahrenheit) {
>     float celcius = fahrenheitToCelcius(fahrenheit);
>     float kelvin = celciusToKelvin(celcius);
>     return kelvin;
>   }
> }
> ```
> 
> Press the green **Run** button.
> 
> ```bash
> Calculate to convert!
> 50 degrees Fahrenheit is 10.0 degrees Celcius
> 20 degrees Celcius is 68.0 degrees Fahrenheit
> 10 degrees Celcius is 283.15 degrees Kelvin
> 500 degrees Fahrenheit is 533.15 degrees Kelvin
> 0 degrees Fahrenheit is 255.37222 degrees Kelvin
> ```
{: .solution}

{% include links.md %}
