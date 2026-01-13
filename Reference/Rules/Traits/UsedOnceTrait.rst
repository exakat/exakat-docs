.. _traits-usedoncetrait:

.. _used-once-trait:

Used Once Trait
+++++++++++++++

  Trait should promote code reuse and be used multiple time. A trait that is used once might be as well merged into its host class, and removed. This is currently overengineered code.

.. code-block:: php
   
   <?php
   
   trait t {
       function foo() {}
   }
   
   class x {
       // This expression may be replaced by the foo method definition
       use t;
   }
   ?>

+----------+---------+---------+----------------------------------------------------------------------------+
| Name     | Default | Type    | Description                                                                |
+----------+---------+---------+----------------------------------------------------------------------------+
| timeUsed | 2       | integer | Maximal number of trait usage, before the trait is considered enough used. |
+----------+---------+---------+----------------------------------------------------------------------------+


Connex PHP features
-------------------

  + `code-reuse <https://php-dictionary.readthedocs.io/en/latest/dictionary/code-reuse.ini.html>`_
  + `overenginereed <https://php-dictionary.readthedocs.io/en/latest/dictionary/overenginereed.ini.html>`_


Suggestions
___________

* Inline the trait with its calling class or trait
* Use the trait in another class or trait




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/UsedOnceTrait                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


