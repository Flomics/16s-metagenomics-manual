Usage
=====

.. _input:

Input
------------

When submitting a job to the 16S pipeline, you will be presented with the following screen:

.. image:: images/launch_screen.png
  :width: 400
  :alt: Launch screen options from Stratus 16S pipeline


Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

