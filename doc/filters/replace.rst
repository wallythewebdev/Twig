``replace``
===========

The ``replace`` filter replaces placeholders in a string (the placeholder
format is free-form):

.. code-block:: twig

    {{ "I like %this% and %that%."|replace({'%this%': fruit, '%that%': "oranges"}) }}
    {# if the "fruit" variable is set to "apples", #}
    {# it outputs "I like apples and oranges" #}

    {# using % as a delimiter is purely conventional and optional #}
    {{ "I like this and --that--."|replace({'this': fruit, '--that--': "oranges"}) }}
    {# outputs "I like apples and oranges" #}
    
    {# Variables can be used for dynamic replacement by wrapping the variable name in () #}
    {% set var = "value" %}
    {{ "Replace a --var--"|replace({'--var--': (var) }) }}
    {# outputs "Replace a value" #}

Arguments
---------

* ``from``: The placeholder values as a hash

.. seealso::

    :doc:`format<format>`
