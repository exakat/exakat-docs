.. _structures-inconsistentconcatenation:

.. _inconsistent-concatenation:

Inconsistent Concatenation
++++++++++++++++++++++++++

  Concatenations happens within a string or using the dot operator. Using both is an inconsistent way of writing concatenations.

Switching methods of concatenation, sometimes in the same expression, is `error <https://www.php.net/error>`_ prone. The reader gets confused, and may miss important information. 



There are some situations where using concatenation are compulsory : when calling a constant, or a function, or make use of the escape sequence. Those are ignored in this analysis.

.. code-block:: php
   
   <?php
   
       //Concatenation
     $consistent = $a . 'b'. $c;
   
       //Interpolation
     $consistentToo = "{$a}b$c";
   
       // Concatenation and interpolation
     $inconsistent = $a . "b$c";
   
       // Concatenation and interpolation too
     $consistentThree = <<<CONSISTENT
   {$a}b$c
   CONSISTENT;
   
       // Concatenation and interpolation collisions
     $collision = theClass::CONSTANTE . "b{$c}".number_format($t, 2).' $CAD'."\n";
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InconsistentConcatenation                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | concat                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-structures-inconsistentconcatenation`                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


