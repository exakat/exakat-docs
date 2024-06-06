.. _functions-multipleidenticalclosure:

.. _multiple-identical-closure:

Multiple Identical Closure
++++++++++++++++++++++++++

  Several closures are defined with the same code. 

It may be interesting to check if a named function could be defined from them.
This analysis also reports functions and methods that look like the closures : they may be considered for switch.

.. code-block:: php
   
   <?php
   
   // the first squares, with closure
   $squares= array_map(function ($a) {return $a * $a; }, range(0, 10) );
   
   // later, in another file...
   // another identical closure 
   $squaring = function ($x) { return $x * $x; };
   foo($x, $squaring);
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.


Suggestions
___________

* Create a function with the body of those closures, and replace the closures by the function's name.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MultipleIdenticalClosure                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


