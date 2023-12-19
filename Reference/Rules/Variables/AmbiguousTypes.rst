.. _variables-ambiguoustypes:

.. _ambiguous-types-with-variables:

Ambiguous Types With Variables
++++++++++++++++++++++++++++++

  The same variable is assigned various types, in different methods. This means that one may expect the same named variable to behave differently in different context.


.. code-block:: php
   
   <?php
   
   function foo() {
   	$i = 1;
   	$user = new User();
   }
   
   function goo() {
   	$i = 2; // $i is always an integer
   	$user = new Propect();  // Sometimes $user is a User, and sometimes it is a Propect
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/AmbiguousTypes                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


