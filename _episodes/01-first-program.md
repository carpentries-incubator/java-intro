---
title: Your first Java program
teaching: 0
exercises: 0
questions:
- "What does the simplest program look like in Java?"
objectives:
- "Writing the most basic program that can run in Java."
- "Identify the different parts of the program and explain their purpose."
- "Know what a class is."
- "Know why we need ```main(String[] args)```."
keypoints:
- "What is a class?"
- "What is the purpose of public static void ```main(String[] args)?```"
- "What is an object?"
- "What does 'instantiate' mean?"
- "What is the naming convention of classes?"
- "What should the filename be in which a class is saved?"
- "What will the filename be of a compiled class?"
---

## Smallest possible program

We mentioned on our introductory page that Java is a **class based** and **object oriented** language. You can think of a class as a "blue print". If you are an architect and the computer is the builder, then the architect (the programmer) will provide the builder (the computer) with a blue print (the class) to build (instantiate) something (an object).

Let's create a class called HelloWorld (the blue print). This class will be used to build a program that is going to print "Hello World" on the screen. The name of the file in which the class is saved **HAS** to be the same as the name of the class ending with the extention ```.java```. Usually we would call this program HelloWorld, but because of the way repl.it works, we have to call it Main. So we have to create a file called Main.java. To the Java compiler it doesn't matter what you call it but convention is to call it something meaningful so that someone else (or you when you come back to it tomorrow) can infer from the name what it will do.

Type the following code into the editor:

```java
/** 
 * Define a class
 **/
class Main {

  // The entry level to a Java program is a method called ```main```
  // Don't forget the ```String[] args``` in the parenthesis. 
  public static void main(String[] args) {
    // The next line will print the characters between the quotes to the screen
    System.out.println("Hello World");
  }
}
```
Let's look at the program line by line.

1. The first three lines are comments. You can start a comment block with ```/**``` and end it with ```**/```. Everything in between these markers will be considered to be comments. The ```*``` at the beginning of the second line is purely for readability.
1. Line 4 defines the name of the class. By convention, classnames start with a capital letter. The name of the file in which the class is saved must be the same as the class name and it has to end in ```.java```. Curly braces are used to indicate the beginning and ending of a structure. So the left curly brace after the classname, Main, indicates the beginning of the class while the right curly brace on line 12 closes it.
1. The 5th line is empty. It is used purely for readability, the compiler will ignore any empty lines
1. Lines 6 and 7 are single line comments. If you start a line with ```//```, the rest of the line will be ignored and considered to be a comment.
1. It is important to understand line 8. However, trying to explain the meaning of each word in this line will be difficult at this point but it will become clearer as we go through the workshop. The main thing is to know that a Java program needs at least one class with this ```main``` method in it. It is like the front door to the program. When you ask the Java Runtime Environment (JRE) to run your program, it will look for this ```main``` method. The word ```public``` tells the JRE that the method is visible outside the class. The meaning of this will become clearer when we write several classes to work together. If it was called private, the method would only be visible to the code inside the class itself. We'll leave the word ```static``` for later but it is important to know that it is needed for this specific method. You also need the ```String[] args``` in the curly brackets - it's meaning will also become clear in the following episodes. As before, the curly braces are used to define the begin and end of a code block, which in this case is a **method**. 


The code now has to be compiled before it can run. In repl.it, above the editor there is a button with the word ```Run``` and a small green arrow. Press the button to compile and run the program. In the console, next to the editor, repl.it displays the commands for compiling and running. 

```bash
> javac -classpath .:/run_dir/junit-4.12.jar:target/dependency/* -d . Main.java
> java -classpath .:/run_dir/junit-4.12.jar:target/dependency/* Main
Hello world!
>
```
You could do all of this manually but usually your IDE, as repl.it is doing now, will take care of it. The first line compiles the program. The second line runs the program and the third line is the output of the program.

> ## Exercise
> You can add as many System.out.println statements as you want. Experiment a bit and print some things on the screen.
{: .challenge}

> ## Solution
> ```java 
> class Main {
>   public static void main(String[] args) {
>     System.out.println("I like to eat my peas with honey;");
>     System.out.println("I've done it all my life.");
>     System.out.println("It makes the peas taste funny,");
>     System.out.println("But it keeps them on the knife.");
>  }
> }
> ```
> Press the green **Run** button.
> ```bash
> $ javac -classpath .:/run_dir/junit-4.12.jar:target/dependency/* -d . Main.java
> $ java -classpath .:/run_dir/junit-4.12.jar:target/dependency/* Main
> I eat my peas with honey;
> I've done it all my life.
> It makes the peas taste funny,
> But it keeps them on the knife.
> ```
{: .solution}

> ## Challenge - Run the program again without compiling it again
> The repl.it editor is divided into the left, middle and right panes. The right pane has two tabs, one for the ```Console``` and one for the ```Shell```.
> 1. Select the ```Shell``` tab
> 1. You should see the bash prompt:
> 
> ```bash
> ~/01HelloWorld$
>```
> 1. Type ```ls``` and enter to get a listing of files in the directory.
> 1. You should see two files:
>   - Main.class
>   - Main.java
> 1. Main.class is the compiled version of the program. To run it type the following at the command prompt:
> 
> ```bash
> java Main
> ```
> What happens?

{: .challenge}

> ## Summary
> 
> 1. Java code is organised in classes. A program consists of one or more classes.
> 1. One of the classes of a program must have a method called ```main(String[] args)```. The JRE needs the ```main``` method to run a program.
> 1. During `runtime` (i.e. when you run the program), classes get **instantiated** which means that the memory required to run a class is reserved and the code for that class is loaded into that memory. This chunk of reserved memory is then called an object.
> 1. By convention classnames start with a capital.
> 1. Classes are saved in a file with the same name as the class and with the extension ```.java```.
> 1. When a class is compiled, the compiled code will be saved in a filename with the same name as the class but with a ```.class``` extension.

{: .discussion}

{% include links.md %}

