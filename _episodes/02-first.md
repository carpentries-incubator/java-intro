---
title: "Our first program"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "Writing the most basic Java program that will run."
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---
If you followed the instructions so far you should now have a file called App.java with the following bit of code in it:

```java
public class App {
    public static void main(String[] args) throws Exception {
        System.out.println("Hello, World!");
    }
}

```
VSC added this basic outline for you. Do you remember that we said Java is a *class based* programming language? Well, here you can see that a class was created for you. Let's recreate this manually.

First create a new file. Make sure you have selected `src` inside `java-intro-program`. Click on File, New File and enter the name HelloWorld.java. When you press enter. VSC will create the file `HelloWorld.java` with the following code int it:
```java
public class HelloWorld {
    
}
```
This is the most basic piece of code you have in Java, but you can yet run it in any way because it is just an empty class. To be able to run a Java program you have to specify the entry point. We do this by creating a method called `main` in the class. Add the following code between the curly brackets

```
    public static void main(String[] args) {

    }
```

The program should now look like this:
```java
public class HelloWorld {
        public static void main(String[] args) {
            
        }
}

{% include links.md %}

