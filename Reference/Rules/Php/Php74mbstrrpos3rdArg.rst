.. _php-php74mbstrrpos3rdarg:

.. _mb\_strrpos()-third-argument:

mb_strrpos() Third Argument
+++++++++++++++++++++++++++

  Passing the encoding as 3rd parameter to `mb_strrpos() <https://www.php.net/mb_strrpos>`_ is deprecated. Instead pass a 0 offset, and encoding as 4th parameter.

.. code-block:: php
   
   <?php
   
   // Finds the position of the last occurrence of of a string in a string, starting at position 10
   $extract = mb_strrpos($haystack, $needle, 10, 'utf8');
   
   // This is the old behavior. Here, the offset will be 0, by default
   $extract = mb_strrpos($haystack, $needle, 'utf8');
   ?>

See also mb_strrpos().


Suggestions
___________

* Remove usage of mb_strrpos() 3rd parameter.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/Php74mbstrrpos3rdArg                                                                                                                                                                |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.8.9                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                     |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                                                              |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


