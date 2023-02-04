Introducing methods
===================

You have been using methods for quite a while now. All those times where you've
created the main method and have een calling the ``print`` method to output
results from the terminal.

You will write code for this section in a different directory to the one used for the Hello World program. Follow the following instructions below to do so: 

1. Create a new directory called ``Methods`` under your ``ValaProjects`` directory.
2. Under the ``Methods``  directory you have just created, create a new file called ``main.vala``.

Methods in more detail
----------------------

As explained previously in the Hello World section, a method is a block of 
code that contain code for the program to execute when called.

Now let's create a program that makes use of a method that you create and call.

First, let's start with a Hello World program

.. code-block:: vala
    :caption: main.vala

    public static void main () {
        print ("Hello World\n");
    }

Now let's create a method to move the printing logic outside of the ``main`` method.

.. code-block:: vala
    :emphasize-lines: 1-3,6
   
    public static void say_something () {
        print ("Hello World\n");
    }

    public static void main () {
        say_something ();
    }

The output of this program will still be:

.. code-block:: console

    Hello World

Updating our new method
-----------------------

One of the benefits of using methods is that we can do this
