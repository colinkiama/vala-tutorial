Booleans and if-statements
--------------------------

In this section we'll:

- Teach you about boolean values and variables
- Introuduce a way to change the flow of a program based on a boolean value

Introudction to Booleans
~~~~~~~~~~~~~~~~~~~~~~~~

Light bulbs ultimately have two, mutually-exclusive states: ``on`` and ``off``. When a light bulb is ``on``, it has emits light. When a light bulb is ``off``, there is no light.

Sometimes, in our programs, we need to represent two mutually exclusive states. The boolean data type (``bool``) is how you we can do this.

Instead of ``on`` and ``off``, we'd use the ``true`` and ``false`` boolean values to represent two mutually-exclusive states.

We can store boolean values in variables:

.. code-block:: vala
   
   bool is_on = false;

Now, you'll write some actual code involving booleans.

Setup steps:
1. Create a new directory called ``Booleans`` under your ``ValaProjects`` directory.
2. Create a new file called ``main.vala`` inside the ``Booleans`` directory you created.

In ``main.vala``, write the following code:

.. code-block:: vala
   :caption: main.vala
   
   public static void main () {
       print ("Hello!\n");
   }

If you compile and run the program, it will simply print "Hello!".

If-statement
~~~~~~~~~~~~

Let's make your program more interesting now.

Above the ``print`` method, add declare a boolean variable set to ``false``:

.. code-block:: vala
   :caption: main.vala - Boolean variable added

   public static void main () {
   	   bool should_print = false;
       print ("Hello!\n");
   }

We want the program above to only print "Hello" when the value of ``should_print`` is set to ``true``. You can do this by using a control statement called an ``if-statement``.

Update ``main.vala`` so that it wraps the print call with an ``if-statement``, that checks if the value of ``should_print`` is ``true``

.. code-block:: vala
   
   public static void main () {
      bool should_print = false;

      if (should_print == true) {
         print ("Hello!\n");
      }
   }

Now compile and your code.

As you can see, nothing happens. Let's break down why: 


