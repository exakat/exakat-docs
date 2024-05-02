.. _classes-methodsignaturemustbecompatible:

.. _method-signature-must-be-compatible:

Method Signature Must Be Compatible
+++++++++++++++++++++++++++++++++++

  Make sure methods signature are compatible.

PHP generates the infamous Fatal `error <https://www.php.net/error>`_ at execution : ``Declaration of FooParent\:\:Bar() must be compatible with FooChildren\:\:Bar()``

.. code-block:: php
   
   <?php
   
   class x {
       function xa() {}
   }
   
   class xxx extends xx {
       function xa($a) {}
   }
   
   ?>

Suggestions
___________

* Fix the child class method() signature.
* Fix the parent class method() signature, after checking that it won't affect the other children.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MethodSignatureMustBeCompatible                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | typehint, type-covariance, type-contravariance                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


