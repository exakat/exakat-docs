.. _namespaces-unresolveduse:

.. _unresolved-use:

Unresolved Use
++++++++++++++

  The following use instructions cannot be resolved to a known class, interface, trait, constant or function. They should be dropped or fixed.

A known class, interface, trait, constant or function is defined in PHP (standard), an extension, a stub or the current code.
Use expression are options for the current namespace.

.. code-block:: php
   
   <?php
   
   namespace A {
       // class B is defined
       class B {}
       // class C is not defined
   }
   
   namespace X/Y {
   
       use A/B;  // This use is valid
       use A/C;  // This use point to nothing.
   
       new B();
       new C();
   }
   
   ?>

See also `Using namespaces: Aliasing/Importing <https://www.php.net/manual/en/language.namespaces.importing.php>`_.


Suggestions
___________

* Remove the use expression
* Fix the use expression




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/UnresolvedUse                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | namespace, use                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unresolved-use <https://github.com/dseguy/clearPHP/tree/master/rules/no-unresolved-use.md>`__                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


