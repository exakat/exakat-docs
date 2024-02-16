.. _classes-finalclass:

.. _final-class-usage:

Final Class Usage
+++++++++++++++++

  List of all final classes being used.

final may be applied to classes and methods.


.. code-block:: php
   
   <?php
   class BaseClass {
      public function test() {
          echo 'BaseClass::test() called'.PHP_EOL;
      }
      
      final public function moreTesting() {
          echo 'BaseClass::moreTesting() called'.PHP_EOL;
      }
   }
   
   class ChildClass extends BaseClass {
      public function moreTesting() {
          echo 'ChildClass::moreTesting() called'.PHP_EOL;
      }
   }
   // Results in Fatal error: Cannot override final method BaseClass::moreTesting()
   ?>

See also `Final Keyword <https://www.php.net/manual/en/language.oop5.final.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/Finalclass                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | final                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


