.. _performances-staticcalldontneedobjects:

.. _static-call-may-be-truly-static:

Static Call May Be Truly Static
+++++++++++++++++++++++++++++++

  `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ calls are allowed on objects. Although, when using typehinting, it is better to use the actual type, and allow PHP to prepare this at compilation time, not at execution time.

When the typehint is an interface or an abstract class, then the object may hold a different type : those cases are omitted.
This is a micro-optimisation. The call is very fast, but will gain another 1/3 with a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ syntax.

.. code-block:: php
   
   <?php
   
   function foo(A $a, $b) {
       // This could use \A instead of $a
       echo $a::class;
   
       // This will be arbitrary and needs $b
       echo $a::class;
   }
   
   ?>

Suggestions
___________

* Use the actual typehint of the parameter or property
* Use a parent of the typehint of the parameter or property




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/StaticCallDontNeedObjects                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Features     | static                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


