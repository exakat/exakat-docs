.. _classes-fossilizedmethod:

.. _fossilized-method:

Fossilized Method
+++++++++++++++++

  A method is fossilized when it is overwritten so often that changing a default value, a return type or an argument type is getting difficult.

This happens when a class is extended. When a method is overwritten once, it may be easy to update the signature in two places. The more methods are overwriting a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ method, the more difficult it is to update it.

This analysis counts the number of times a method is overwritten, and report any method that is overwritten more than 6 times. This threshold may be configured.

.. code-block:: php
   
   <?php
   
   class x1 {
       // foo1() is never overwritten. It is easy to update.
       function foo1() {}
   
       // foo7() is overwritten seven times. It is hard to update.
       function foo7() {}
   }
   
   // classes x2 to x7, all overwrite foo7();
   // Only x2 is presente here.
   class x2 extends x1 {
       function foo7() {}
   }
   
   ?>

+------------------------+---------+---------+---------------------------------------------------------------------------------+
| Name                   | Default | Type    | Description                                                                     |
+------------------------+---------+---------+---------------------------------------------------------------------------------+
| fossilizationThreshold | 6       | integer | Minimal number of overwriting methods to consider a method difficult to update. |
+------------------------+---------+---------+---------------------------------------------------------------------------------+



See also `Method fossilization <https://www.exakat.io/en/method-fossilisation/>_`.


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/FossilizedMethod                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.6                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | fossilized-method                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


