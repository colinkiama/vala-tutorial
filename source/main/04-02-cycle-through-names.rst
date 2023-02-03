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

Now let's use the ``for`` loop to make each parrot repeat the entered phrase.

.. code-block:: vala
    :emphasize-lines: 8-14

    public static void main () {
        string[] parrot_names = {"Jurg", "Raffaele", "Dani"};

        print ("Enter your phrase: ");

        string input = stdin.read_line ();

        if (input == null) {
            return;
        }

        for (int i = 0; i < parrot_names.length; i++) {
            print (@"$(parrot_names[i]) says: $input\n");
        }
    }

After compilng this program, for the input "It is what it is",
the following output will be displayed: 

.. code-block:: console

    Jurg says: It is what it is
    Raffaele says: It is what it is
    Dani says: It is what it is


