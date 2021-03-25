---
title: "Numbers"
teaching: 0
exercises: 0
questions:
- "How can we print numbers on the screen?"
- "When is a number just text and when is it an actual numeric value?"
- "How do I do calculations on numbers?"
objectives:
- "Distinguish between strings and values."
- "Do basic calculations on values."
- "Know what an operator is."
keypoints:
- "What is a string?"
- "What is concatenation?"
---

What would a programming language be without the ability to manipulate numbers? So let's try a couple of thing to discover how Java works with numbers and characters.

Start by creating a new repl called ```02.Numbers```. As before, repl.it will create a file called Main.java for you with the "Hello World" code in it. Change the code to look as follows:

```java
class Main {
  public static void main(String[] args) {
    System.out.println("Print the number ten: 10");
  }
}
```

When you run the program it should print the following on the screen:

```bash
Print the number ten: 10
```

> ## Exercise
> - Insert the following statement after the third line ```System.out.println("Print the number ten: " + 10);```
> ```java
> class Main {
>   public static void main(String[] args) {
>     System.out.println("Print the number ten: 10");
>     System.out.println("Print the number ten: " + 10);
>   }
> }
> ```
> - Compile and run the program again.
>
> Does the output of line 3 look different to the output of line 4?
> What is the difference between the two statements?
{: .challenge}

> ## Solution
> From the user's point of view there is no difference but, to the compiler there is a difference. Characters that are enclosed in quotes are considered to be a string. In the first case the digits of the number 10 are considered to be characters. Java uses something called **Unicode** which is a standard for encoding text expressed in most of the world's writing systems. Each character in Unicode has a unique number. In the second statement the number 10 is not in quotes and is therefore considered to be an integer value. However, the compiler has to convert the number to a string before it can concatenate it to the string in the quotes. The compiler does this automatically.
{: .solution}

Let's try something different. Change your program to look as follows and compile and run it again:

```java
class Main {
  public static void main(String[] args) {
    System.out.println("Print ten plus ten: 10 + 10");
    System.out.println("Print ten plus ten: " + 10 + 10);
    System.out.println("Print ten plus ten: " + (10 + 10));
  }
}
```

```bash
Print ten plus ten: 10 + 10
Print ten plus ten: 1010
Print ten plus ten: 20
```

> ## Discussion
> Why do you think we are getting this output?
{: .discussion}

{% include links.md %}

