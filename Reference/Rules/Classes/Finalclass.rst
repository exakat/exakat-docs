.. _classes-finalclass:

.. _final-class-usage:

Final Class Usage
+++++++++++++++++

.. meta::
	:description:
		Final Class Usage: This rule lists of all final classes in use in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Final Class Usage
	:twitter:description: Final Class Usage: This rule lists of all final classes in use in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Final Class Usage
	:og:type: article
	:og:description: This rule lists of all final classes in use in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Final Class Usage.html
	:og:locale: en
This rule lists of all final classes in use in the code. 

The ``final`` option may be applied to classes and methods: this rule only reports classes.

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

Related PHP errors 
-------------------

  + `Cannot override final method %s::%s() <https://php-errors.readthedocs.io/en/latest/messages/cannot-override-final-%25s%3A%3A%25s%28%29-with-%25s%3A%3A%25s%28%29.html>`_



Connex PHP features
-------------------

  + `final <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/Finalclass                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


