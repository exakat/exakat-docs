.. _functions-nobooleanasdefault:

.. _no-boolean-as-default:

No Boolean As Default
+++++++++++++++++++++

  Default values should always be set up with a constant name.

Class constants and constants improve readability when calling the methods or comparing values and statuses.

.. code-block:: php
   
   <?php
   
   const CASE_INSENSITIVE = true;
   const CASE_SENSITIVE = false;
   
   function foo($case_insensitive = true) {
       // doSomething()
   }
   
   // Readable code 
   foo(CASE_INSENSITIVE);
   foo(CASE_SENSITIVE);
   
   
   // unreadable code  : is true case insensitive or case sensitive ? 
   foo(true);
   foo(false);
   
   ?>

See also `FlagArgument <https://www.martinfowler.com/bliki/FlagArgument.html>`_ and `Clean code: The curse of a boolean parameter <https://medium.com/@amlcurran/clean-code-the-curse-of-a-boolean-parameter-c237a830b7a3>`_.


Suggestions
___________

* Use constants or class constants to give value to a boolean literal
* When constants have been defined, use them when calling the code
* Split the method into two methods, one for each case




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoBooleanAsDefault                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.0                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | boolean, default-value                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openconf-functions-nobooleanasdefault`                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


