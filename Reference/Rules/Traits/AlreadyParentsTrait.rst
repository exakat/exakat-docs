.. _traits-alreadyparentstrait:

.. _already-parents-trait:

Already Parents Trait
+++++++++++++++++++++

  Trait is already used a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_'s class or trait. There is no use to include it a second time, so one of them can be removed.

.. code-block:: php
   
   <?php
   
   trait ta {
       use tb;
   }
   
   trait t1 {
       use ta;
       use tb; // also used by ta
   }
   
   class b {
       use t1; // also required by class c
       use ta; // also required by trait t1
   }
   
   class c extends b {
       use t1;
   }
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.


Suggestions
___________

* Eliminate the trait in the parent class
* Eliminate the trait in the child class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/AlreadyParentsTrait                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | trait                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


