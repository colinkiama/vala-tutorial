Enums and switch statements
===========================

In this section we'll:

- Introduce the switch statement
- Introudce enum values
- Showcase how switch statements and enums work well togeter

Switch Statements
-----------------

In the last section, we introuduced ``if`` statements:

.. code-block:: vala
   
   bool is_on = true;
   if (is_on) {
      print ("The light bulb is on\n");
   }

However, there as you've seen with ``if`` statements, when you have several potential branches, it can become quite cumbersome to write:

.. code-block:: vala

   string lang_name = "Vala";

   print ("Programming language facts:\n\n");

   if (lang_name == "Vala") {
      print ("Vala first appeared in 2006\n");
   } else if (lang_name == "Rust") {
       print ("Rust's Mascot is a red crab\n");
   } else if (lang_name == "C++") {
       print ("First editiion of C++ was released around since 1985\n");
   } else if (lang_name == "C") {
       print ("C was created by Dennis Ritche")
   } else {
       print ("Goodbye\n");
   }

Notice that we're always checking the value of the ``lang_name`` variable with an eqality check ``lang_name == value``.

Rather than writing out the eqaulity check, for the same variable, every time, you can use a ``switch`` statement instead.

.. code-block:: vala
   
   string lang_name = "Vala";
   
   switch (lang_name) {
      case "Vala":
         print ("Vala first appeared in 2006\n");
         break;
      case "Rust":
         print ("Rust's Mascot is a red crab\n");
         break;
      case "C++":
         print ("First editiion of C++ was released around since 1985\n");
         break;
      case "C":
         print ("C was created by Dennis Ritche\n")
         break;
      default:
         print ("Goodbye\n");
         break;
   }

.. tip::
   
   The `elementary coding style <https://docs.elementary.io/develop/writing-apps/code-style>`_ recommends using a ``switch`` statement
   when checking the value of the same variable more than twice, in ``if`` statements.

``switch`` statements runs a section of code based on the value passed into it.
In this case, ``lang_name`` was passed into te ``switch`` statement so the value "Vala", will be compared against.

Each ``case`` is like an equality check for the value passed in. ``case "Vala"`` behaves similarly to ``if (lang_name == "Vala")``.
Then after the ``:`` of each ``case`` the section of code to run on the matching case is written.

To signal the end of the code to run, a ``break`` statement is used.

``default`` beahves like ``else``. It runs when no other cases match the value passed in. 

Switch Fallthrough
~~~~~~~~~~~~~~~~~~

In ``if`` statements, to run the same block of code based on a set of matching values, you would do somethhing like this:

.. code-block:: vala

   string lang_name = "Vala";
   
   if (lang_name == "Vala" || lang_name == "C") {
      print ("C was created by Dennis Ritche\n")
      print ("Vala compiles to C\n");
   }

As you can imagine, this can become pretty cumbersome to write as you add more matching values.

In ``switch`` statements, the syntax for this is much more concise, making it easier to expand the matching potential values over time:

.. code-block:: vala
   :emphasize-lines: 3-8
   
   string lang_name = "Vala";
   
   switch (lang_name) {
      case "Vala":
      case "C":
         print ("C was created by Dennis Ritche\n")
         print ("Vala compiles to C\n");
         break;
      case "Rust":
         print ("Rust's Mascot is a red crab\n");
         break;
      case "C++":
         print ("First editiion of C++ was released around since 1985\n");
         break;
      default:
         print ("Goodbye\n");
         break;
   }

The "Vala" ``case`` has the "C" ``case`` directly under it. It runs the section of code under the "C" ``case``.
The same code would run if ``lang_name`` was set to "C" too. This is called the ``switch`` statement's **fallthrough** behaviour.

Enums
-----

Now, you'll write some actual code involving ``switch`` statements and value type called an Enumeration (``enum``).

Setup steps:

1. Create a new directory called ``Switch`` under your ``ValaProjects`` directory.
2. Create a new file called ``main.vala`` inside the ``Switch`` directory you created.

In ``main.vala``, write the following code:

.. code-block:: vala
   :caption: main.vala
   
   public static void main () {
      string lang_name = "Vala";
      
      switch (lang_name) {
         case "Vala":
         case "C":
            print ("C was created by Dennis Ritche\n")
            print ("Vala compiles to C\n");
            break;
         case "Rust":
            print ("Rust's Mascot is a red crab\n");
            break;
         case "C++":
            print ("First editiion of C++ was released around since 1985\n");
            break;
         default:
            print ("Goodbye\n");
            break;
   }

Now, if you compile and run the code, it should print the following lines:

.. code-block::

    C was created by Dennis Ritche
    Vala compiles to C

