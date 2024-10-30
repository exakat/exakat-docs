.. _structures-alwaysfalse:

.. _comparison-is-always-the-same:

Comparison Is Always The Same
+++++++++++++++++++++++++++++

  Based on the incoming type of arguments, the comparison always yields the same value. The whole condition might be useless.

.. code-block:: php
   
   <?php
   
   function foo(array $a) {
       // This will always fail
       if ($a === 1) {
           
       } elseif (is_int($a)) {
       
       }
   
       // This will always succeed
       if ($a !== null) {
           
       } elseif (is_null($a)) {
           
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Suggestions
___________

* Remove the constant condition and its corresponding blocks
* Make the constant condition variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AlwaysFalse                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                   |
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


