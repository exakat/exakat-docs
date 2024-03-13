.. _exceptions-possibletypeerror:

.. _possible-typeerror:

Possible TypeError
++++++++++++++++++

  Report possible errors when a string is given to a int or float typed container. 

That `error <https://www.php.net/error>`_ will be emitted when strict_types is active, or if the string cannot be formatted into a float or an int. Otherwise, the code works as intended.



It is recommended to set a try/catch around those expressions, to catch them.

.. code-block:: php
   
   <?php
   
   // This is OK, as the string will be successfully turned into a float
   foo("12.34");
   
   // This is KO, as the string will not bet turned into a float
   foo("12.34a");
   
   function foo(float $price) {
   	intdiv($price, 3);
   }
   
   ?>

See also `TypeError <https://www.php.net/manual/en/class.typeerror.php>`.


Suggestions
___________

* Add the try expression around the assignation, to catch the error
* Validate the incoming value to ensure it can be converted to the target type
* Cast the value to int or float




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/PossibleTypeError                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | typeerror                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


