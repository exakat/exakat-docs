.. _classes-uselessconstantoverwrite:

.. _useless-constant-overwrite:

Useless Constant Overwrite
++++++++++++++++++++++++++

  A class constant is defined in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and child class, with the same value. One of them is useless and may be removed.


.. code-block:: php
   
   <?php
   
   class x {
   	const A = 1;
   	const B = 1;
   }
   
   class y extends x {
   	// A is the same as in the parent class.
   	const A = 1;
   	// B has a new value, so it is important.
   	const B = 2;
   }
   
   ?>

Suggestions
___________

* Remove the parent constant
* Remove the child constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessConstantOverwrite                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


