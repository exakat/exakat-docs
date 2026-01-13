.. _structures-identicalonbothsides:

.. _identical-on-both-sides:

Identical On Both Sides
+++++++++++++++++++++++

  Operands should be different when comparing or making a logical combination. Of course, the value each operand holds may be identical. When the same operand appears on both sides of the expression, the `result <https://www.php.net/result>`_ is know before execution.

.. code-block:: php
   
   <?php
   
   // Trying to confirm consistency
   if ($login == $login) {
       doSomething();
   }
   
   // Works with every operators
   if ($object->login( ) !== $object->login()) {
       doSomething();
   }
   
   if ($sum >= $sum) {
       doSomething();
   }
   
   //
   if ($mask && $mask) {
       doSomething();
   }
   
   if ($mask || $mask) {
       doSomething();
   }
   
   ?>
Connex PHP features
-------------------

  + `if-then <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Suggestions
___________

* Remove one of the alternative, and remove the logical link
* Modify one of the alternative, and make it different from the other




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IdenticalOnBothSides                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpmyadmin-structures-identicalonbothsides`, :ref:`case-humo-gen-structures-identicalonbothsides`                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


