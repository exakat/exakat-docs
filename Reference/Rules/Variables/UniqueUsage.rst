.. _variables-uniqueusage:

.. _single-use-variables:

Single Use Variables
++++++++++++++++++++

  This is the list of variables that are written, then read, and only used once.

Single-use variables may be trimmed down, and the initial expression may be used instead.

Single-use variables may improve readability, when the final expression grows too much with the extra expression. 


.. code-block:: php
   
   <?php
   
   function foo($d) {
       $a = 1;     // $a is used twice
       $b = $a + 2;  // $b is used once
       $c = $a + $b + $d; // $c is also used once
       // $d is an argument, so it's OK.
       
       retrun $c;
   }
   
   ?>
Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Merge the two expressions into one larger
* Make a second use of the variable
* Inline the code of the expression instead of the variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/UniqueUsage                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.0                                                                                                                   |
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


