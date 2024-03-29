.. _classes-rewrotefinalclassconstant:

.. _rewrote-final-class-constant:

Rewrote Final Class Constant
++++++++++++++++++++++++++++

  Final class constants can't be rewriten in a child class. 

It is possible to write code that lints, when the classes are in different files. Such overwrites will only be detected at execution time.


.. code-block:: php
   
   <?php
   
   class x {
   	final const A = 1;
   	const B = 1;
   }
   
   class y extends x {
   	const A = 1;
   	const B = 1;
   }
   
   ?>

Suggestions
___________

* Remove the final keyword
* Remove the rewritten constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/RewroteFinalClassConstant                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | final                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


