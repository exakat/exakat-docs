.. _classes-implementedmethodsarepublic:

.. _implemented-methods-must-be-public:

Implemented Methods Must Be Public
++++++++++++++++++++++++++++++++++

  Class methods that are defined in an interface must be public. They cannot be either private, nor protected.
This `error <https://www.php.net/error>`_ is not reported by lint, and is reported at execution time.

.. code-block:: php
   
   <?php
   
   interface i {
       function foo();
   }
   
   class X {
       // This method is defined in the interface : it must be public
       protected function foo() {}
       
       // other methods may be private
       private function bar() {}
   }
   
   ?>

See also `Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_ and `Interfaces - the next level of abstraction <https://phpenthusiast.com/object-oriented-php-tutorials/interfaces>`_.


Suggestions
___________

* Make the implemented method public




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ImplementedMethodsArePublic                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | method, visibility                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


