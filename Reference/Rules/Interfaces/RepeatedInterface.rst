.. _interfaces-repeatedinterface:

.. _repeated-interface:

Repeated Interface
++++++++++++++++++

  A class should implements only once an interface. An interface can only extends once another interface. In both cases, `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes or interfaces must be checked.

PHP accepts multiple times the same interface in the ``implements`` clause. In fact, it doesn't do anything beyond the first implement. 


.. code-block:: php
   
   <?php
   
   use i as j;
   
   interface i {}
   
   // Multiple ways to reference an interface
   class foo implements i, \i, j {}
   
   // This applies to interfaces too
   interface bar extends i, \i, j {}
   
   ?>


This code may compile, but won't execute.

See also `Object Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_ and `The Basics <https://www.php.net/manual/en/language.oop5.basic.php>`_.


Suggestions
___________

* Remove the interface usage at the lowest class or interface




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/RepeatedInterface                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | interface                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


