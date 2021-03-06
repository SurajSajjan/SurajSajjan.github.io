---
title: "Performance and Code Complexity Comparison between Julia and C++"
date: 2019-07-30
tags: [Julia, C++, Programming, High Performance Computing]
header:
  image: "/images/Torontoflatironcondos.jpg"
categories: Programming
---

Working with Julia and C++.

**Introduction:** In this project, we write code for a couple of problems using two of the programming languages namely, C++ and Julia. We shall discuss the complexity of writing code in each language and also compare the performance of each of the language to the other.
We are using atom IDE on CentOS for writing C++ codes. We are using Jupyter notebook with Julia on Windows 10 for writing Julia code.

Before we start with the analysis, let us look at some of the Pros and Cons of C++ and Julia.

**C++:**

Pros: It is one of the foundation languages which has a huge community and following. There are libraries present for almost all kinds of tasks. C++ allows us to out the large arrays on “heap” which helps in avoiding “stack overflow”. C++ was also one of the earliest programming languages to leverage the concept of Object-Oriented Programming (OOP) and includes inheritance, polymorphism, encapsulation, class, and abstraction. Most of the code written in C work on C++. It is one of the best ways to understand algorithms. It is one of the highly portable languages and is the language most developers choose for multi-device, multi-platform app development. It also allows exception handling and function overloading. Due to its power and efficiency, it has a range of applications from GUI applications to 3D graphics for games to real-time scientific simulations.
Cons: The standard used allows many things that can result in unexpected behavior. There is no boundary check on arrays. It also allows improper type conversion. This could result in an inexperienced programmer to corrupt his memory. It does not do a lot of memory management, forcing the developers to do the majority of it themselves. The C++ object-oriented programming is unnecessarily basic compared to other languages like Java which have better and more flexible systems. C++ programming can be quite complicated as the syntax is complex and the standard library is small. This makes it challenging and hard to learn to code in it. It is also syntactically strict. The syntax has very less flexibility making it difficult to write readable user-friendly code. The higher-level features such as GUIs, threading, and networking depend on the operating system making it unstandardized. This forces the programmer to either include different versions of code or include outside libraries which have already done so.

**Julia:**

Pros: Julia reaches the speed of compiled languages such as C++ and Fortran. It provides dynamism of high-level languages such as Python as well as mathematical notations found in MATLAB. Julia also provides the statistical ease of languages such as R as well as the ease of use of Python. The combination of these elements makes Julia a very powerful language. Julia a multiple dispatch language. Any function call made may be dispatched to different functions. Another feature of Julia is its speed. Julia is capable of compiling code on the fly. It combines the method of interpreting languages such as Python which transform the code into bytecode with compiled languages such as C which compiles its code into machine code and then running the generated executable. This enables Julia to run at similar speeds of C. Packages are an import part of Julia like R. Julia has a built-in package manager containing over 1900 registered packages. Julia’s amazing feature is its parallelism. The programmer can parallelize directly from the command line by calling the desired script with the desired number of cores. It is also capable of sending different threads directly from code.
Cons: Julia came into the picture in the year 2012. Due to its short existence, the support to the language is also relatively limited. As of yet, few libraries exist wit the community being quite small. The design of Julia probably comes from MATLAB, making it unnatural to interface C ++ or Python. Julia arrays are 1-indexed which can be can catch users off guard, the ones who are used to coding in Python or C++.
Julia list comprehensions lack the ability to use conditionals, unlike Python. It can be done with for loops and if/else as normally done. The matrices in Julia are accessed column-major compared to Python’s NumPy where the matrices are accessed row-order. This can affect the design decisions on how to iterate over matrices effectively in memory. The dictionaries in Julia are hashed differently than Python dictionaries making them slower in many cases.

**Analyis and Observations:**

Code to perform two different tasks are written in both Julia and C++:

* Addition of all the element of the matrix and then the addition of only the diagonal elements followed by multiplication of the first matrix with another of the same dimensions.
We perform the above task for a 3X3 Matrix followed by a 1000X1000 Matrix.

* Determining the value of y at an x using the 4th order Runge-Kutta method.

The first thing to be noted is how simple and easy to understand the code of Julia is. The first problem was to calculate the sum of elements of the first matrix, the sum of elements of its diagonals as well as multiply it with another matrix. In Julia, we needed only 8 lines of code for the whole problem whereas it was 134 lines of code in C++ for the same computation. We found that C++ was significantly faster than Julia. Both for a small matrix as well as a matrix of dimension 1000X1000, C++ was faster. Almost twice as fast for the larger matrices. However, in the second problem where we calculated the value of y for a given x using 4th order Range-Kutta method, we found that Julia was significantly faster compared to C++. We observe that for computational intense problems like the first problem with multiple matrices with a large number of rows and columns, C++ seems to work faster. For relatively less computationally intense problems like the second problem, Julia lives up to its name to bring the compiling speeds of C and the ease of writing code of Python together.

The complete report along with the code for the above programs can be found here: [**JuliaVsCPP**](https://github.com/SurajSajjan/JuliaVsCPP){:target="_blank" rel="noopener" }