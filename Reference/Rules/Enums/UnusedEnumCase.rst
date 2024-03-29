.. _enums-unusedenumcase:

.. _unused-enumeration-case:

Unused Enumeration Case
+++++++++++++++++++++++

  Those are enumeration cases which are defined, yet not used.


.. code-block:: php
   
   <?php
   
   enum x {
       case A;
       case C;
       
       const F = 1;
   }
   
   function foo(x $a) {}
   
   foo(x::A);
   
   ?>


The `error <https://www.php.net/error>`_ message when the case is missing mentions the class constant : this is because enumeration cases and class constants use the same configuration. They are only distinguished by their definition, which, here, does not exists.

Suggestions
___________

* Use the case in the code
* Remove the case in the code
* Fix the name of the case
* Turn the case in a constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Enums/UnusedEnumCase                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Dead code <ruleset-Dead-code>`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | enum                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`undefined-enumcase`                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


