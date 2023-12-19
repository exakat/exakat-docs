.. _arrays-nullboolean:

.. _null-or-boolean-arrays:

Null Or Boolean Arrays
++++++++++++++++++++++

  Null and booleans are valid PHP array base. Yet, they only produces ``null`` values. They also did not emits any warning until PHP 7.4.

This analysis has been upgraded to cover int and float types too.


.. code-block:: php
   
   <?php
   
   // outputs NULL
   var_dump(null[0]);
   
   const MY_CONSTANT = true;
   // outputs NULL
   var_dump(MY_CONSTANT[10]);
   
   ?>

See also `Null and True <https://twitter.com/Chemaclass/status/1144588647464951808>`_.


Suggestions
___________

* Avoid using the array syntax on null and boolean
* Avoid using null and boolean on constant that are expecting arrays




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Arrays/NullBoolean                                                                                                      |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.8.6                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.4                                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                               |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Features         | null, boolean, array                                                                                                    |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


