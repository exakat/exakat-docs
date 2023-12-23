.. _exceptions-coulddropvariable:

.. _could-drop-variable:

Could Drop Variable
+++++++++++++++++++

  Suggest removing the variable in catch clause where the variable is not used. The type of the `exception <https://www.php.net/exception>`_ is sufficient to make the catch clause work. Although, it is recommended to use the caught `exception <https://www.php.net/exception>`_, for chaining or logging, for example. 

.. code-block:: php
   
   <?php
   
   try {
   	doSomething();
   } catch(Exception1 $e) {
   	// No usage of $e : just drop it from the clause
   } catch(Exception2 $e2) {
   	// $e2 is caught and used. 
   	echo $e2->getMessage();
   }
   
   ?>

Suggestions
___________

* remove the unused variable




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CouldDropVariable                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Dead code <ruleset-Dead-code>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------+
| Features     | catch                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------+
| Available in |                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------+


