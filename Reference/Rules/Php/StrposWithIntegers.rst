.. _php-strposwithintegers:

.. _strpos()-with-integers:

strpos() With Integers
++++++++++++++++++++++

  `strpos() <https://www.php.net/strpos>`_ used to accept integer as second argument, and turn them into their ASCII equivalent. This was deprecated in PHP 7.x, and dropped in 8.0.


.. code-block:: php
   
   <?php
   
   strpos('abc ', 32);
   // PHP 8.0+ : false, 32 is not found
   // PHP 7.4- : 3, 32 is turned into space, then found
   
   ?>


It is recommended to use casting to ensure the variable is actually strings, and `strpos() <https://www.php.net/strpos>`_ behaves as expected.

Suggestions
___________

* Add a cast to make the data string
* Test the data to be a string before usage




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/StrposWithIntegers                                                                                                  |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.5.2                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                              |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                    |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


