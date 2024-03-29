.. _structures-calltimepassbyreference:

.. _calltime-pass-by-reference:

Calltime Pass By Reference
++++++++++++++++++++++++++

  PHP doesn't allow when a value is turned into a reference at functioncall, since PHP 5.4. 

Either the function use a reference in its signature, either the reference won't pass.

.. code-block:: php
   
   <?php
   
   function foo($name) {
       $arg = ucfirst(strtolower($name));
       echo 'Hello '.$arg;
   }
   
   $a = 'name';
   foo(&$a);
   
   ?>

See also `Passing by Reference <https://www.php.net/manual/en/language.references.pass.php>`_.


Suggestions
___________

* Make the signature of the called method accept references
* Remove the reference from the method call
* Use an object instead of a scalar




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CalltimePassByReference                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | by-value, by-reference                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


