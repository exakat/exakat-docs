.. _php-returnwithparenthesis:

.. _return-with-parenthesis:

Return With Parenthesis
+++++++++++++++++++++++

  return statement doesn't require parenthesis. PHP tolerates them with return statement, but it is recommended not to use them. 

From the PHP Manual : 'Note: Note that since return is a language construct and not a function, the parentheses surrounding its argument are not required and their use is discouraged.'.

.. code-block:: php
   
   <?php
   
   function foo() {
       $a = rand(0, 10);
   
       // No need for parenthesis
       return $a;
   
       // Parenthesis are useless here
       return ($a);
   
       // Parenthesis are useful here: they are needed by the multplication.
       return ($a + 1) * 3;
   }
   
   ?>

See also `PHP return(value); vs return value; <https://stackoverflow.com/questions/2921843/php-returnvalue-vs-return-value>`_ and `return <https://www.php.net/manual/en/function.return.php>`_.

Connex PHP features
-------------------

  + `return-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/return-value.ini.html>`_


Suggestions
___________

* Remove the parenthesis




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ReturnWithParenthesis                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


