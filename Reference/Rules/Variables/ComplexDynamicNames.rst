.. _variables-complexdynamicnames:

.. _complex-dynamic-names:

Complex Dynamic Names
+++++++++++++++++++++

  Avoid using expressions as names for variables or methods. 

There are no place for checks or flow control, leading to any rogue value to be used as is. Besides, the expression is often overlooked, and not expected there : this makes the code less readable.

It is recommended to build the name in a separate variable, apply the usual checks for existence and validity, and then use the name.


.. code-block:: php
   
   <?php
   
   $a = new foo();
   
   // Code is more readable
   $name = strolower($string);
   if (!property_exists($a, $name)) {
       throw new missingPropertyexception($name);
   }
   echo $a->$name;
   
   // This is not check
   echo $a->{strtolower($string)};
   
   ?>


This analysis only accept simple containers, such as variables, properties.

See also  `Dynamically Access PHP Object Properties with $this <https://drupalize.me/blog/201508/dynamically-access-php-object-properties>`_.


Suggestions
___________

* Extract the expression from the variable syntax, and make it a separate variable.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/ComplexDynamicNames                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | dynamic-variable                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


