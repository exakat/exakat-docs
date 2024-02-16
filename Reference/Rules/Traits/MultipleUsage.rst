.. _traits-multipleusage:

.. _multiple-usage-of-same-trait:

Multiple Usage Of Same Trait
++++++++++++++++++++++++++++

  The same trait is used several times. One trait usage is sufficient.






PHP doesn't raise any `error <https://www.php.net/error>`_ when traits are included multiple times.

.. code-block:: php
   
   <?php
   
   // C is used twice, and could be dropped from B
   trait A { use B, C;}
   trait B { use C;}
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.


Suggestions
___________

* Remove any multiple traits from use expressions
* Review the class tree, and remove any trait mentioned multiple times




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/MultipleUsage                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | trait                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-traits-multipleusage`                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


