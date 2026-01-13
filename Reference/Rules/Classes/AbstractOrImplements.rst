.. _classes-abstractorimplements:

.. _abstract-or-implements:

Abstract Or Implements
++++++++++++++++++++++

  A class must implements all abstract methods of it parents, or be abstract too. 

PHP detect such `error <https://www.php.net/error>`_ when all classes are loaded: in a code source where classes are split by files, such `error <https://www.php.net/error>`_ it won't be detected until execution, where PHP stops with a Fatal `Error <https://www.php.net/error>`_ : ``Class BA contains 1 abstract method and must therefore be declared abstract or implement the remaining methods (A\:\:aFoo)``.

.. code-block:: php
   
   <?php
   
   abstract class Foo { 
       abstract function FooBar();
   }
   
   // This is in another file : php -l would detect it right away
   
   class FooFoo extends Foo { 
       // The method is not defined. 
       // The class must be abstract, just like Foo
   }
   
   ?>

See also `Class Abstraction <https://www.php.net/abstract>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Class+BA+contains+1+abstract+method+and+must+therefore+be+declared+abstract+or+implement+the+remaining+methods+%28A%3A%3AaFoo%29.html>`_



Connex PHP features
-------------------

  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_
  + `implements <https://php-dictionary.readthedocs.io/en/latest/dictionary/implements.ini.html>`_
  + `lazy-loading <https://php-dictionary.readthedocs.io/en/latest/dictionary/lazy-loading.ini.html>`_


Suggestions
___________

* Implements all the abstract methods of the class
* Make the class abstract




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AbstractOrImplements                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.3                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-classes-abstractorimplements`                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


