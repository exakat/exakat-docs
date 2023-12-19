.. _php-staticclassusage:

.. _class:

\:\:class
+++++++++

  PHP has a special class constant to hold the name of the class : ``class`` keyword. It represents the class name that is used in the left part of the operator.

Using ``\:\:class`` is safer than relying on a string. It does adapt if the class's name or its namespace is changed'. It is also faster, though it is a micro-optimisation. 

It is introduced in PHP 5.5.


.. code-block:: php
   
   <?php
   
   use A\B\C as UsedName;
   
   class foo {
       public function bar( ) {
           echo ClassName::class; 
           echo UsedName::class; 
       }
   }
   
   $f = new Foo( );
   $f->bar( );
   // displays ClassName 
   // displays A\B\C 
   
   ?>


Be aware that ``\:\:class`` is a replacement for `__CLASS__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ magic constant.

See also `Class Constant <https://www.php.net/manual/en/language.oop5.constants.php>`_.


Suggestions
___________

* Use ::class whenever possible. That exclude any dynamic call.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/StaticclassUsage                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | coalesce                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


