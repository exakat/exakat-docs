.. _functions-nodefaultforreference:

.. _no-default-for-referenced-parameter:

No Default For Referenced Parameter
+++++++++++++++++++++++++++++++++++

  Parameters with reference should not have a default value. 

When they have a default value, that default value is not a reference, and it will not have impact on the calling context. 

Then, the parameter behaves like a reference when the argument is provided, and not as a reference when the parameter is not provided. This makes sense : no parameter in, no parameter out.

.. code-block:: php
   
   <?php
   
   function foo(&$i = 1) {
   	++$i;
   }
   
   // $i is 1, but it is not available in the calling context
   foo(); 
   
   // $i is 1, but it is not available in the calling context
   $i = 1;
   foo($i); 
   
   echo $i; // $i is now 2
   
   ?>

Suggestions
___________

* Remove the reference
* Make that parameter a local variable
* Remove the default value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoDefaultForReference                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | reference                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


