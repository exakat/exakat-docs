.. _classes-unresolvedinstanceof:

.. _unresolved-instanceof:

Unresolved Instanceof
+++++++++++++++++++++

  The `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ operator doesn't confirm if the compared class exists. 

It checks if an variable is of a specific class. However, if the referenced class doesn't exist, because of a bug, a missed inclusion or a typo, the operator always fails, without a warning. 


.. code-block:: php
   
   <?php
   
   namespace X {
       class C {}
       
       // This is OK, as C is defined in X
       if ($o instanceof C) { }
   
       // This is not OK, as C is not defined in global
       // instanceof respects namespaces and use expressions
       if ($o instanceof \C) { }
   
       // This is not OK, as undefinedClass
       if ($o instanceof undefinedClass) { }
   
       // This is not OK, as $class is now a full namespace. It actually refers to \c, which doesn't exist
       $class = 'C';
       if ($o instanceof $class) { }
   }
   ?>


Make sure the following classes are well defined.

See also `Instanceof <https://www.php.net/manual/en/language.operators.type.php>`_.


Suggestions
___________

* Remove the call to instanceof and all its dependencies.
* Fix the class name and use a class existing in the project.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnresolvedInstanceof                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Dead code <ruleset-Dead-code>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Features     | instanceof                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unresolved-instanceof <https://github.com/dseguy/clearPHP/tree/master/rules/no-unresolved-instanceof.md>`__                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-classes-unresolvedinstanceof`                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------+


