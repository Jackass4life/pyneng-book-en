Glossary
========

argument
--------

An argument is the actual value (data) that is passed to a function
(or method) when it is called.

attribute
---------

An attribute is a variable associated with an object. Attributes store
the state of an object and are accessed using dot notation.

iterator
--------

An iterator is an object that returns its elements one at a time.

From Python's perspective, it is any object that has a ``__next__``
method. This method returns the next element if it exists, or raises a
StopIteration exception when there are no more elements.

In addition, an iterator remembers which element it stopped at in the
last iteration.

In Python, every iterator has an ``__iter__`` method — that is, any
iterator is an iterable from which an iterator can be obtained. This
method simply returns the iterator itself.

iteration
---------

Iteration is a general term that describes the procedure of taking
elements of something one at a time.

More generally, it is a sequence of instructions that is repeated a
certain number of times or until a specified condition is met.

iterable
--------

An iterable is an object from which an iterator can be obtained.

In Python, the ``iter()`` function is responsible for obtaining an
iterator:

.. code:: python

    In [1]: lista = [1, 2, 3]

    In [2]: iter(lista)
    Out[2]: <list_iterator at 0xb4ede28c>

The ``iter()`` function works on any object that has an ``__iter__``
method or a ``__getitem__`` method.

The ``__iter__`` method returns an iterator. But if this method is
absent, ``iter()`` checks whether there is a ``__getitem__`` method —
a method that allows elements to be obtained by index.

If the ``__getitem__`` method is present, an iterator is returned that
traverses the elements using an index (starting from 0).

In practice, the presence of ``__getitem__`` means that all sequences
of elements are iterables — for example, list, tuple, string.

method
------

A method is a function that belongs to a specific object, and is
accordingly called in relation to that object.

For example, ``print`` is a function:

.. code:: python

    In [11]: print('test')
    test

While ``append`` is a list method. Accordingly it can only be called
on an object that is a list:

.. code:: python

    In [12]: list1 = [1, 2, 3]

    In [13]: list1.append(4)

object
------

In Python, everything is an object. The official definition is an entity
that has some state and certain behaviour.

Examples of objects: list, string, file, and so on.

For example, a file object can be created like this:

.. code:: python

    In [1]: f = open('output.py')

    In [2]: f
    Out[2]: <_io.TextIOWrapper name='output.py' mode='r' encoding='UTF-8'>

This object has the following methods and attributes:

.. code:: python

    In [3]: print([m for m in dir(f) if not m.startswith('_')])
    ['buffer', 'close', 'closed', 'detach', 'encoding', 'errors', 'fileno', 'flush', 'isatty', 'line_buffering', 'mode', 'name', 'newlines', 'read', 'readable', 'readline', 'readlines', 'seek', 'seekable', 'tell', 'truncate', 'writable', 'write', 'writelines']

The object ``f`` here represents the actual file output.py, and
contains the methods and attributes that Python supports for files.

parameter
---------

A parameter is a variable used when defining a function.

sequence
--------

A sequence is an ordered collection of elements that supports index-based
access and has a defined length. Examples: list, tuple, string.

function
--------

A function is a block of code that returns a value. A function can also
accept arguments that affect the execution of the code in the function
body.

Example function:

.. code:: python

    In [14]: def f(a, b):
        ...:     return a+b
        ...:

Function ``f`` has two parameters — ``a`` and ``b``. It returns the sum
of these parameters.

When called with arguments 5 and 10, it returns 15, which is assigned to
the variable ``result``:

.. code:: python

    In [15]: result = f(5, 10)

    In [16]: result
    Out[16]: 15
