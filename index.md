---
layout: lesson
root: .  # Is the only page that doesn't follow the pattern /:path/index.html
permalink: index.html  # Is the only page that doesn't follow the pattern /:path/index.html
---

No prior knowledge of Java or any other programming language is required for this lesson. The lesson is aimed at researchers wishing to write programs in Java for the purposes of gathering or analysing their data.

# Background
The Java programming language is a **class based**, **object-oriented** programming language. The meaning of these terms will be explained during the lesson. Java was designed to be a general-purpose programming language intended to write once, run anywhere (WORA). This means that once written and compiled it should run on any platform that supports Java without the need for recompilation. A Java program requires the Java Virtual Machine to be installed. The syntax of the Java language is similar to that of C/C++.

You might wonder why one would choose to write a program in Java. Python is a very popular language, why don't we all just use that? Or for that matter, why don't we just all use C/C++? Each of these languages have advantages and disadvantages. If written correctly, C/C++ code would probably give you the fastest and most efficient program but it is also very easy to write bad code. C/C++ programs also have to be compiled specifically for the platform and operating system they will be running on. 

Python is an "interpreter", which means you can run the code as you write it - it does not have to be compiled. So, as long as there is a Python interpreter for the platform/operating system you work on, you should theoretically be able to take a program and run it anywhere. However, there is on big problem. Most Python programs rely on several libraries or modules and if those are not installed on your computer, they will have to be installed before you can run the program. If these requirements are not properly specified (i.e. the library and the version and all its dependencies) it could take you hours or even days/weeks to get the program running if you can get it running at all! Because the Python is an interpreter it is also significantly slower than programs written in C/C++ and in some cases it is not feasible to write something in Python as it will just take too long to run.

Java fits nicely between C/C++ and Python with regards to the issues mentioned. It is a compiled language but with a difference. Java is compiled to bytecode which requires a runtime environment to run. Once the Java program is compiled it will run on any computing platform that has the **Java Runtime Environment** (JRE) available. Like C++, Java is object-oriented but with some safety features built in so that, unlike C/C++, you are less likely to develop bad code that will lead to instability and memory leaks. But, because it is compiled it will run much faster than Python. Java will have a higher learning curve than Python but lower than C/C++. Programs such as Eclipse, IntelliJ and Visual Studio Code (VSC) are referred to as IDEs (Integrated Development Environments). We don't need to use them but they do make our lives much easier. They offer features such as syntax highlighting, auto-indentation, and code completion. repl.it is an online environment that gives us the same functionality as the IDEs and for the sake of uniformity across learner environments we will be using it during the workshop.


> You can have a look at the different IDEs on the following websites:
> - [Eclipse](https://www.eclipse.org/ide/)
> - [IntelliJ](https://www.jetbrains.com/idea/)
> - [Netbeans IDE](https://netbeans.org/)
> - [Visual Studio Code](https://code.visualstudio.com/)
>
>
> In your web browser, make your way to [https://replit.com/](https://replit.com/).
{: .prereq}

# Getting Started

To get started follow the directions on the "Setup" page which will guide you through signing up and selecting a Java environment in replit.com.

{% include links.md %}
