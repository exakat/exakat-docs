.. _structures-yodacomparison:

.. _yoda-comparison:

Yoda Comparison
+++++++++++++++

  Yoda comparison is a way to write conditions which places literal values on the left side. 


.. code-block:: php
   
   <?php
     if (1 == $a) {
       // Then condition
     } 
   ?>


The objective is to avoid mistaking a comparison to an assignation. If the comparison operator is mistaken, but the literal is on the left, then an `error <https://www.php.net/error>`_ will be triggered, instead of a silent bug. 


.. code-block:: php
   
   <?php
       // error in comparison! 
       if ($a = 1) {
           // Then condition
       } 
   ?>
 
.

See also `Yoda Conditions <https://en.wikipedia.org/wiki/Yoda_conditions>`_ and `Yoda Conditions: To Yoda or Not to Yoda <https://knowthecode.io/yoda-conditions-yoda-not-yoda>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/YodaComparison                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


