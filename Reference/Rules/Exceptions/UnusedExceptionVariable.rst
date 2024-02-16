.. _exceptions-unusedexceptionvariable:

.. _unused-exception-variable:

Unused Exception Variable
+++++++++++++++++++++++++

  The variable from a catch clause is not used. It is expected to be used, either by chaining the `exception <https://www.php.net/exception>`_, or logging the message.

In PHP 8.0, this variable may be omitted. 


.. code-block:: php
   
   <?php
   
   try{
       doSomething();
   } catch (A $a) {
       // $a is caught, but not used here
   } catch (B $b) {
       // $b is caught, and used
       log($b->getMessage());
   } catch (C) {
       // Caught and ignored (PHP 8.0 +)
   }
   
   ?>

Suggestions
___________

* Drop the variable in the clause expression (PHP 8.0 and more recent)
* Chain the exception
* Log the exception message




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/UnusedExceptionVariable                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | exception                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


