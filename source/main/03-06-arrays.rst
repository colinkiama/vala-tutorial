Arrays
======

You've learned about several data types so far but what if you wanted to store
a collection of them in one variable?

You will write code in this section in a different directory. Follow the instruction below: 

1. Create a new directory called ``Arrays`` under your ``ValaProjects`` directory.
2. Under the ``Arrays``  directory you have just created, create a new file called ``main.vala``.

Introducing Arrays
------------------

Arrays allow you to store a collection of values of the same data type.

An array is declared by giving a type name followed by ``[]`` and 
created by using the ``new`` operator.

Let's try creating an array now:

.. code-block:: vala
    :caption: main.vala

    public static void main () {
        int[] my_array = new int[3];
    }

The number within the square brackets ``[]`` is the size of the array.

.. note:: 

    Elements of value types such as ``int`` will have their default value.
    For the ``int`` type, the value would be ``0``.

    However for reference types like ``string``, no strings will be created.
    Just an array to store the strings in. This behaviour applies to the object type too. 
    If you write ``Object[] a = new Object[10]``, no objects will be created, 
    just the array to store them in.


You can set the value of an array method by getting a rerefence to the element's location
using it's index in the array. 

Array indexes in Vala are zero-indexed so the first element in the array is referenced by 0.
The second element is reference by an index of 1, and so forth.

Here we'll set the first, second and third element of the ``my_array`` as: ``1``, ``2`` and ``3`` respectively:

.. code-block:: vala
    
    public static void main () {
        int[] my_array = new int[3]; // {0, 0, 0}

        my_array[0] = 1; // my_array = {1, 0 ,0}
        my_array[1] = 2; // my_array = {1, 2, 0}
        my_array[2] = 3; // my_array = {1, 2, 3}
    }

However, if you know all the values that you want the array to have initially,
you can declare the array with the values:

.. code-block:: vala
    
    public static void main () {
        int[] my_array = {1, 2, 3};
    }

Notice that you don't need to write the array's size anymore. The compiler can
infers that from the values you've listed the array's delcaration.

To see the values in an array, we use the use the reference each element by its
array index.

.. code-block:: vala
    
    my_array[0] // 1

You can't print the whole array writing something like ``print("%s", my_array)``.

Instead, you can loop through each element in the array by incrementing through
array indexes. 

We'll use the length of array, which can be obtained by the length member variable 
e.g. ``int count = a.length.``:

.. code-block:: vala
    :emphasize-lines: 4-7

    public static void main () {
        int[] my_array = {1, 2, 3};

        print ("My array:\n");
        for (int i = 0; i < my_array.length; i++) {
            print (@"$(my_array[i])\n");
        }
    }


Summary
-------

Congratualations! You've now finished this chapter.

To recap, you've learned:

- About variables and what they are used for
- Different types of data types like integers and boolean
- How to change the flow of programs using control statements such as: ``if`` and ``switch``.
- How to perform loops using loop statements such as ``while`` and ``for``.
- How to store a collection of a specific data type using arrays

The next chapter will be a project that will use some of the topics you've learned so far.

Now would be a good idea to revise and experiment with the topics we've covered in this tutorial up until now to improve your understanding with them.

Now, on to the next chapter!
