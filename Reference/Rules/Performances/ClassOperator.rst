.. _performances-classoperator:

.. _scope-resolution-operator:

Scope Resolution Operator
+++++++++++++++++++++++++

  The scope resolution operator `\:\:class` is faster than a call to `get_class() <https://www.php.net/get_class>`_ function.

It is also possible to replace `get_class()` by `static\:\:class` to get the name of the calling class.

.. code-block:: php
   
   <?php
   
   $a = new stdClass();
   
   echo $a::class;
   
   // identical to 
   echo get_class($a);
   
   class x {
       function foo() { echo static::class; }
   }
   
   class y extends x {}
   
   // static will resolve to y here
   (new y)->foo();
   
   ?>

See also `get_class <https://www.php.net/manual/fr/function.get-class.php>`_..

Connex PHP features
-------------------

  + `scope-resolution-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/scope-resolution-operator.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Use the `::class` operator instead of the call to get_class()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/ClassOperator                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


