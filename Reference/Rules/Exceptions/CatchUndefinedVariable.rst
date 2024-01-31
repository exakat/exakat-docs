.. _exceptions-catchundefinedvariable:

.. _catch-with-undefined-variable:

Catch With Undefined Variable
+++++++++++++++++++++++++++++

  Always initialize every variable before the try block, when they are used in a catch block. If the `exception <https://www.php.net/exception>`_ is raised before the variable is defined, the catch block may have to handle an undefined variable, leading to more chaos.

.. code-block:: php
   
   <?php
   	$a = 1;
   	try {
   	    mayThrowAnException();
   	    $b = 2;
   	} catch (\Exception $e) {
   	    // $a is already defined, as it was done before the try block
   	    // $b may not be defined, as it was initialized after the exception-throwing expression
   	    echo $a + $b;
   	}
   ?>

See also `catch <https://www.php.net/manual/en/language.exceptions.php#language.exceptions.catch>`_ and `Non-capturing exception catches in PHP 8 <https://www.amitmerchant.com/non-capturing-exception-catches-php8/>`_.


Suggestions
___________

* Always define the variable used in the catch clause, before the try block.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CatchUndefinedVariable                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                   |
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


