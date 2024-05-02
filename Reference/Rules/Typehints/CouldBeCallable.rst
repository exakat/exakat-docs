.. _typehints-couldbecallable:

.. _could-be-callable:

Could Be Callable
+++++++++++++++++

  Mark arguments and return types that can be set to ``callable``.

The analysis also reports properties that could be 'callable', although PHP doesn't allow that configuration.
Note that properties cannot be callable. It reports a compilation `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // Accept a callable as input 
   function foo($b) {
       // Returns value as return
       return $b();
   }
   
   ?>

See also `Callbacks / callables <https://www.php.net/manual/en/language.types.callable.php>`_.


Suggestions
___________

* Add `callable` typehint to arguments or returntypes.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeCallable                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Typechecks <ruleset-Typechecks>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | callback, callable                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


