.. _classes-incompatiblesignature:

.. _incompatible-signature-methods:

Incompatible Signature Methods
++++++++++++++++++++++++++++++

  Methods should have the same signature when being overwritten.

The same signatures means the children class must have : 

+ the same name
+ the same visibility or less restrictive
+ the same typehint or removed
+ the same default value or removed
+ a reference like its `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_

This problem emits a fatal `error <https://www.php.net/error>`_, for abstract methods, or a warning `error <https://www.php.net/error>`_, for normal methods. Yet, it is difficult to lint, because classes are often stored in different files. As such, PHP do lint each file independently, as unknown `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes are not checked if not present. Yet, when executing the code, PHP lint the actual code and may encounter a fatal `error <https://www.php.net/error>`_.


.. code-block:: php
   
   <?php
   
   class a {
       public function foo($a = 1) {}
   }
   
   class ab extends a {
       // foo is overloaded and now includes a default value for $a
       public function foo($a) {}
   }
   
   ?>

See also `Object Inheritance <https://www.php.net/manual/en/language.oop5.inheritance.php>`_.


Suggestions
___________

* Make signatures compatible again




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IncompatibleSignature                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`LintButWontExec <ruleset-LintButWontExec>`            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-classes-incompatiblesignature`                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


