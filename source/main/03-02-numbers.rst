Numbers
=======

In this section we'll:

- Teach you about some numeric data types
- Explain what operators are
- Help you write programs using variables with numeric data types

You will write code for this section in a different directory to the one used for the Hello World program. Follow the following instructions below to do so: 

1. Create a new directory called ``Numbers`` under your ``ValaProjects`` directory.
2. Under the ``Numbers``  directory you have just created, create a new file called ``main.vala``.

Numeric Data Types
------------------

In the last section, we showed an example of a variable:

.. code-block:: vala
   
   string my_name = "Sara";

In your ``main.vala`` file, create a `main` method with, an ``int`` variable assignment, in the `main` method's body:

.. code-block:: vala
   :caption: main.vala - ``int`` variable declaration.

   public static void main () {
       int num = 42;
   }

The ``num`` variable of you've created in the line above stores `int` values and you have set the value of it to ``42``.

You can print the value of ``num`` by adding using the ``print`` method. Add this line below where you wrote the ``num`` variable's delcaration:

.. code-block:: vala
   :caption: main.vala - Print value of ``num``
   :emphasize-lines: 3

   public static void main () {
      int num = 42;
      print ("Value of num: %d\n", num);
   }



