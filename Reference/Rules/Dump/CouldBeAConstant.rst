.. _dump-couldbeaconstant:

.. _could-be-a-constant:

Could Be A Constant
+++++++++++++++++++

  This analysis detects literal values that make good candidate for constants. 

Candidates needs two characteristics : 

+ Be assigned as a whole to a container (variable, properties, etc.)
+ Be later (or somewhere else) compared to a container. 

Such literal is used as a token, to handle a state. It is set, then read later. Then, a constant, may it be global or class, is important, so that the relationship between the setting and the reading is maintained throughout the life of the application.

Once the literal is converted into a constant, the value of the literal is not important. It could even be turned into an object. 


.. code-block:: php
   
   <?php
   
   const SOME_TOKEN = 'abc';
   
   $a = 'some-token';
   $b = SOME_TOKEN; // same as above, as a constant
   
   function foo($arg) {
       if ($arg === 'some-token') {
       
       }
   
       if ($arg === SOME_TOKEN) {
       
       }
   }
   
   ?>


Not all literals that are set then read may be turned into a constant : there might be overlap in features by frequently used values (such as true, false, 0, 1, ) or simple confusion with a local literal. Also, literals that are used for their value (like 1 in a `$a + 1` expression) are not good candidates.

+---------------+---------+---------+---------------------------------------------------------------+
| Name          | Default | Type    | Description                                                   |
+---------------+---------+---------+---------------------------------------------------------------+
| minOccurences | 1       | integer | Minimal number of occurrences of the literal.                 |
+---------------+---------+---------+---------------------------------------------------------------+
| skipString    | ,.php   | array   | List of omitted string values. For example, the empty string. |
+---------------+---------+---------+---------------------------------------------------------------+
| skipInteger   | 1,-0,-1 | array   | List of omitted integer values. By default, 0, 1 and -1.      |
+---------------+---------+---------+---------------------------------------------------------------+



Suggestions
___________

* Create the constant and replace all connected literals with it. 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CouldBeAConstant                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dump <ruleset-Dump>`                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | constant                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


