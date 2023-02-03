Cycle through names
====================

Add parrots
-----------

First, add an array of names for each parrot:

.. code-block:: vala
    :emphasize-lines: 2

    public static void main () {
        string[] parrot_names = {"Jurg", "Raffaele", "Dani"};

        print ("Enter your phrase: ");

        string input = stdin.read_line ();

        if (input != null) {
            print ("Your phrase: %s\n", input);
        }
    }

