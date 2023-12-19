.. _php-reservedmethods:

.. _reserved-methods:

Reserved Methods
++++++++++++++++

  PHP has reserved all the methods names, starting with two underscores characters ``__``. 

While this is not explicitely enforced, using such names may create future conflict if PHP acquire features that rely on them.

.. code-block:: php
   
   <?php
   
   class x {
   	// One of the reserved and used PHP method
   	function __toString() {} 
   
   	// One potential PHP reserved method
   	function __toArray() {} 
   }
   
   ?>

See also `Magic methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.


Suggestions
___________

* Change the name of the method and avoid prefixing it with ``__``




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ReservedMethods                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | naming, magic method                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


