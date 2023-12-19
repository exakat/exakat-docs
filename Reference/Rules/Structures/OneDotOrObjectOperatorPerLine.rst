.. _structures-onedotorobjectoperatorperline:

.. _one-dot-or-object-operator-per-line:

One Dot Or Object Operator Per Line
+++++++++++++++++++++++++++++++++++

  Rule #4 of Object Calisthenics : Only one -> or . per line.


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


This analysis will also catch the following cases : 


.. code-block:: php
   
   <?php
       // set of multiples (concatenations or properties or methodcalls)
       foo('a' . 'b', 'c'. 'd');
       foo('a' . 'b', $c->d);
   
   ?>


When kept, simple, this rule has some edge cases which are left to the reader.


.. code-block:: php
   
   <?php
   
   $a = 'a' . 'b'
        . 
        'c' . 'd';
   $c = $f->g('e' . 'f');
   
   $e = A::B::D;
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneDotOrObjectOperatorPerLine                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
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


