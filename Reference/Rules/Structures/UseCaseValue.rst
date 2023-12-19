.. _structures-usecasevalue:

.. _use-the-case-value:

Use The Case Value
++++++++++++++++++

  When `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ has branched to the right case, the value of the switched variable is known : it is the case.

This doesn't work with complex expression cases, nor with default. 


.. code-block:: php
   
   <?php
   
   switch($a) {
       case 'a' : 
           // $a == 'a';
           echo $a;
           break;
           
       case 'b' : 
           // $a == 'b';
           echo 'b';
           break;
   }
   
   ?>

Suggestions
___________

* Use the literal value in the case, to avoid unnecessary computation.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseCaseValue                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                   |
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


