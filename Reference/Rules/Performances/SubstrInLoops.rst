.. _performances-substrinloops:

.. _substr()-in-loops:

Substr() In Loops
+++++++++++++++++

  Successive `substr() <https://www.php.net/substr>`_ calls may be replaced by a call to `str_split() <https://www.php.net/str_split>`_. 

It speeds up the processing, and allows the replacement of indefinite loops by a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ call. 


.. code-block:: php
   
   <?php
   
   $bits = str_split($string, 5);
   foreach($bits as $bit) {
   	foo($bit);
   }
   
   $i = 0;
   $s = strlen($string);
   while($i < $s) {
   	// repeating calls to substr during the loop
   	foo(substr($string, $i * 5, 5));
   	$i += 5;
   }
   
   ?>


This is a micro optimisation. It works better on longer strings.

Suggestions
___________

* Use str_split()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SubstrInLoops                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


