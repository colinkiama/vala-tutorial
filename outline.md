# Outline

Important note: 
- Feel free to take inspiration from existing vala programs for the example code project tasks.
- Make sure that a clear, active voice is used thought the tutorial.

## Table of contents

1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
    1.  [Installation](#installation)
    2. [Hello World Program](#hello-world-program)
    3. [Basic Debugging](#basic-debugging)
3. [Data Types and Control Structures](#data-types-and-control-structures)
    1. [Intro to numbers](#intro-to-numbers)
    2. [Booleans and if-statements](#booleans-and-if-statements)
    3. [Enums and Switch Statements](#enums-and-switch-statements)
    4. [Namespaces (Reveal that the data types used so far are from GLib)](#namespaces)
    5. [Loops](#loops)
4. [Parrot Program](#parrot-program)
5. Methods (Introduce asynchronous methods here and variable-length argument lists here too.)
6. Collections
7. Error Handling
8. Object-Oriented Programming (Introduce methods with syntax support here too)
9. Libraries and Build Systems (Valadoc, Valadoc's documentation syntax, Valadoc.org, documentation generation and Meson are introduced here too)
10. Debugging and Testing (Expand on the Debugging section in the old wiki tutorial for now)
11. Multithreading
12. D-Bus
13. Memory Management
14. Profiles
15. Coding Styles (You could also mention vala-lint here too.)
16. Community
17. Epilogue (Congratulate student and point the to further resources. Where could they go next?)

## Introduction

### Why Vala?

* (Explain the language's strengths and incentives for people to learn the language. Start off with brief quotes of Jurg explaining what Vala is in his original first release email then, talk about what the language is like and for today in more detail).

## Getting Started

### Installation

#### Windows Instructions

(These can be copied from the the documentation guide)

#### macOS Instructions

(These can be copied from the the documentation guide)

#### Linux Instructions

(These can be copied from the the documentation guide)

#### Verifying the Installation

- Vala compiler install troubleshooting 
    - Calling compiler with version flag should show a version number
- Explain that the code and features in this tutorial are what was present in Vala 0.56. Code from earlier versions may work but aren't guaranteed to.

### Hello World Program

1. Tell student to copy this a “Hello, World” print statement, inside a static void main block, to their code editor
2. Make them compile the code
3. Verify with them, the output “Hello, World”
4. Break down the program, giving them a chance to learn the language’s syntax
5. Bonus step: Tell the student to run the compile again but with the "compile to C code" flag. Mention that this is C code that Vala generates before it gets compiled to a program binary.

### Basic Debugging (Continues from Hello World Program)

1. Now make the student do a syntax error on purpose e.g print ("Hello" World).
2. Teach them briefly about errors by explaining the compiler error that showed up
3. Explain how to fix the error
4. Make them fix the error
5. Now ask them to update the string so that it greets them e.g "Hello Colin"
6. Introduce comments (Just the single line ones for now)
7. Make student add comment above print statement that describes what it does.
8. Congratulate students
9. Chapter Recap.

## Data Types and Control Structures

### Variables

1. Introduce concept of a variable
    1. Data Type
    2. Identifier
    3. Value
2. Explain reasons for using variables

### Intro to numbers

1. Make student set an integer (Note: you also explain a bit of string formatting here as you need to to use variable arguments and the new line character escape)
2. Print the integer
3. Make students copy and paste math expressions and then print them (introduce them to arithmetic operators)
4. Make students print their own math expression

### Booleans and if-statements

1. Start with a light bulb analogy
2. Now go on to how we can represent one-off states in computers using Booleans (true, false)
3. Print a few Boolean variables
4. Introduce conditional operators (&&, ||, !)
5. Student executes example code that print showcases how the operators behave
6. Introduce if-statement (for performing an action based on a boolean value)
7. Introduce if-else statements
8. Introduce if-else-if statements
9. Introduce if-else-if-else statements (this isn't a typo)

### Enums and Switch Statements

1. Start with an example full of an excessive number of ``else-if`` statements.
2. Introduce switch statements with one of the key benefits of being much more flexible than ``if-statements``. (Perform an action based on the value of string for this example)
3. Introduce enums
4. Showcase how switch statements and enums work well together
5. Show off case-collapse feature (How a set of values can run the same logic). 

### Loops

1. Introduce loops
    1. While loop
    2. Do while loop
    3. For loop

## Parrot Program

1. Introduce constants
2. Make students create for loop with a constant for the end condition part
3. Now make the phrase "Learn Vala, Do Future" be printed on each loop
4. Introduce input and output streams (regarding console input and output)
5. Make students enter a phrase in the program then store it in a variable (make them print it to see)
6. Very briefly introduce arrays. More details will be given later in the tutorial
7. Make the student copy a line that contains a string array of Parrot names
8. Make student modify the loop to print the following using printf formatting "{parrot\_name} says: Learn Vala, Do Future" by looping through array indexes
9. Lastly, make them refactor it by using a foreach loop (the last loop they weren't taught). Explain that because we are always going to go through the whole list and we aren't doing anything unique based on the current position of each name on the list, foreach makes more sense here.
10. Briefly explain the concept of refactoring and the fact that because they changed the loop they've used, now there are many variables they don't need anymore
11. Make students remove those unused variables.
12. Make students verify that the program still works
13. Congrats!


## Methods

1. Remind reader that they've been using methods for a while now - creating the main method and calling the print method (which will be revealed as GLib.print in the Object-oriented programming chapter)
2 Explain what a method is
3. Walk through the creation of a method and calling the method from
4. Add a note that technically these are functions because they aren't part of an instance of a class but in Vala we call functions "methods" anyway.
5. Go into detail about the main entry method and the different ways it can be called and used.