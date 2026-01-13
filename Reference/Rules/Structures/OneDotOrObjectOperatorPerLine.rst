.. _structures-onedotorobjectoperatorperline:

.. _one-dot-or-object-operator-per-line:

One Dot Or Object Operator Per Line
+++++++++++++++++++++++++++++++++++

  Rule #4 of Object Calisthenics : Only one -> or . per line.
This analysis will also catch the following cases : 
When kept, simple, this rule has some edge cases which are left to the reader.

.. code-block:: php
   
   <?php
   
   // Those should be on different lines for readability
   $a->foo()->bar()->getFinal();
   
   $a->foo()
     ->bar()
     ->getFinal();
   
   // Those should be on different lines for readability
   $concatenation = 'a' . 'b' . $c . 'd';
   
   $concatenation = 'a' . 
                    'b' . 
                    $c .
                    'd';
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneDotOrObjectOperatorPerLine                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


