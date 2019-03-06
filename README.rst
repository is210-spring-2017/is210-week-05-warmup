####################
IS 210 Assignment 05
####################
************
Warmup Tasks
************

:College: CUNY School of Professional Studies
:Course-Name: Software Application Programming I
:Course-Code: IS 210

Overview
========

Modules are at the very heart of the Python programming language. Each Python
file created is its own module whether it's imported directly or run on the
command line. In this set of exercises we'll look at modules in isolation.

Instructions
============

The following tasks will either have you interacting with existing files in
the assignment repository or creating new ones on the fly. Don't forget to add
your interpreter directive, utf-8 encoding, and a short docstring with any new
files that you create!

.. important::

    In these exercises, you may, on occasion, come across a task that requres
    you to research or use a function or method not directly covered by the
    course text. Since Python is such a large language it would be impossible
    for the author to have included descriptions of each and every available
    function which would largely duplicate the offical Python documentation.

    A *vital* skill to successful programming is being comfortable searching
    for and using official language documentation sources like the
    `Python String Documentation`_ page. Throughout our coursework we will be
    practicing both the use of the language in practice and the search skills
    necessary to become functional programmers.

Warmup Tasks
============

Task 01: Create a Package
-------------------------

We'll assume you're comfortable with basic module creation and will move
straight on to package creation.

Specifications
^^^^^^^^^^^^^^

#.  Create a package called ``task_01``

#.  Create a module in ``task_01`` named ``peanut``

#.  In ``peanut``, create a constant named ``BUTTER`` and have it return a
    truthy value.

#.  In ``peanut``, create a second constant named ``OIL`` and assign it a
    falsy value

Examples
^^^^^^^^

.. code:: pycon

    >>> import task_01.peanut
    >>> if task_01.peanut.BUTTER: print `I am Truthy`
    'I am Truthy'

    >>> import task_01.peanut
    >>> if not task_01.peanut.OIL: print 'I am Falsy'
    'I am Falsy'

Task 02: Import a Module Namespace
----------------------------------

We'll begin our importation practice by importing a module with its full
namespace. Generally, this is the safest way to import modules though it's not
always the most practical.

Specifications
^^^^^^^^^^^^^^

#.  Create a module called ``task_02``

#.  Import the ``peanut`` module from the ``task_01`` package

#.  Create a new constant in ``task_02`` called, ``TIME`` and assign it the
    value from ``BUTTER`` constant of the ``peanut`` module

Examples
^^^^^^^^

.. code:: pycon

    >>> import task_02
    >>> if task_02.TIME: print 'I am truthy, too!'
    'I am truthy, too!'

Task 03: Copy a Module Attribute
--------------------------------

Our next import adventure has us copying module attributes into the current
namespace.

Specifications
^^^^^^^^^^^^^^

#.  Create a module called ``task_03``

#.  Copy the ``BUTTER`` constant from the ``peanut`` module into the ``task_03``
    namespace

#.  Create a new constant called ``JELLY`` and assign its value from the
    copied ``BUTTER`` attribute

.. warning::

    There is a BIG difference between copying *data* and copying an object or
    attribute from another module. If you've just redeclared the BUTTER
    variable via ``BUTTER =`` you've not achieved the objective of this
    task.

Examples
^^^^^^^^

.. code:: pycon

    >>> import task_03
    >>> True if task_03.BUTTER else False
    True

    >>> task_03.JELLY == task_03.BUTTER
    True

Submission
==========

Your code should be submitted via Blackboard, as a compressed folder containing python files.

.. _GitHub: https://github.com/
.. _Python String Documentation: https://docs.python.org/2/library/stdtypes.html
