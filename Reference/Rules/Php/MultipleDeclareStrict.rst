.. _php-multipledeclarestrict:

.. _multiple-declaration-of-strict\_types:

Multiple Declaration Of Strict_types
++++++++++++++++++++++++++++++++++++

  At least two declare() commands are declaring `strict_types` in one file. Only one is sufficient, and should be the first expression in the file.

Indeed, any `strict_types` set to 1 will have the final word. Setting `strict_types` to 0 will not revert the configuration, wherever is this call made.

.. code-block:: php
   
   <?php 
   declare(strict_types=1);
   declare(strict_types=1);
   
   // rest of the code 
   
   ?>

See also `Declare <https://www.php.net/manual/en/control-structures.declare.php>`_.


Suggestions
___________

* Remove all but one of them. Keep the first one. 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MultipleDeclareStrict                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | declare, strict_types                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


