.. _structures-emptyloop:

.. _empty-loop:

Empty Loop
++++++++++

  This rule reports empty loop. An empty loop has no operation in its main block. 

Some empty loop may have features: they are calling methods in the condition, which may change the status of a resource. 

Empty loop may come from a typo, where a semi colon detach the block from its loop.

.. code-block:: php
   
   <?php
   
   $i = 0;
   // sneaky semi-colon behind the while
   while($i < 10) ; {
   	$i++;
   }
   
   // another sneaky semicolon
   foreach($a as $b) ; 
   {
   	$i++;
   }
   
   // This skips the first empty lines
   $fp = fopen('/path/to/file', 'r');
   while(!($row = fgets($fp))) {
   	
   }
   
   ?>

Suggestions
___________

* Remove the extra semicolon
* Fill the loop with a payload




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EmptyLoop                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | loop                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


