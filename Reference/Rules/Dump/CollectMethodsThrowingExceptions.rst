.. _dump-collectmethodsthrowingexceptions:

.. _collect-methods-throwing-exceptions:

Collect Methods Throwing Exceptions
+++++++++++++++++++++++++++++++++++

  This is a list of all the methods and functions that throw `exception <https://www.php.net/exception>`_.

This rule reports explicit throw's, and doesn't list exceptions passing through : for example, when the `exception <https://www.php.net/exception>`_ is thrown in a sub-call, but not caught yet.

.. code-block:: php
   
   <?php
   
   function foo($a) {
   	if ($a % 2) {
   		throw new Exception('This is not an even number');
   	}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectMethodsThrowingExceptions                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
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


