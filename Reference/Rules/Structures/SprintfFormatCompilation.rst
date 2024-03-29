.. _structures-sprintfformatcompilation:

.. _sprintf-format-compilation:

Sprintf Format Compilation
++++++++++++++++++++++++++

  The `sprintf() <https://www.php.net/sprintf>`_ format used yields an `error <https://www.php.net/error>`_.

This applies to `printf() <https://www.php.net/printf>`_, `sprintf() <https://www.php.net/sprintf>`_, `vprintf() <https://www.php.net/vprintf>`_, `vfprintf() <https://www.php.net/vfprintf>`_, `vsprintf() <https://www.php.net/vsprintf>`_, `sscanf() <https://www.php.net/sscanf>`_, `fscanf() <https://www.php.net/fscanf>`_

.. code-block:: php
   
   <?php
   
       printf('"%we3e"', 123); 
       //Unknown format specifier
   ?>

See also `sprintf <https://www.php.net/manual/en/function.sprintf.php>`_.


Suggestions
___________

* Fix the format




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SprintfFormatCompilation                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | sprintf                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


