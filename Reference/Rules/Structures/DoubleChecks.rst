.. _structures-doublechecks:

.. _double-checks:

Double Checks
+++++++++++++

  Double checks happen when data is checked at one point, and then, checked again, with the same test, in a following call.

Some of the testing may be pushed to the type system, for example `is_int() <https://www.php.net/is_int>`_ and ``int`` type. Others can't, as the check is not integrated in the type system, such as `is_readable() <https://www.php.net/is_readable>`_ and ``string``, for a path. 

The check may be removed from the method, when the method is not called elsewhere without protection. 
Cleaning such structure leads to micro-optimisation.

.. code-block:: php
   
   <?php
   
   if (is_writeable($path)) {
   	foo($path);
   }
   
   function foo(string $path) {
   	// This was already tested
   	if (!is_writeable($path)) {
   		return;
   	}
   }
   
   ?>

Suggestions
___________

* Remove the check in the method
* Remove the check in the caller code
* Use type system




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DoubleChecks                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


