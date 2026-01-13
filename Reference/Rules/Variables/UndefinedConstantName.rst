.. _variables-undefinedconstantname:

.. _undefined-constant-name:

Undefined Constant Name
+++++++++++++++++++++++

  When using the `` syntax for variable, the name used must be a defined constant. It is not a simple string, like 'x', it is an actual constant name.

Interestingly, it is possible to use a qualified name within ``, full or partial. PHP will lint such code, and will collect the value of the constant immediately. Since there is no fallback mechanism for fully qualified names, this ends with a Fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   const x = "a";
   $a = "Hello";
   
   // Display 'Hello'  -> $a -> Hello
   echo ;
   
   // Yield a PHP Warning 
   // Use of undefined constant y - assumed 'y' (this will throw an Error in a future version of PHP)
   echo ;
   
   // Yield a PHP Fatal error as PHP first checks that the constant exists 
   //Undefined constant 'y'
   echo ;
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Undefined+constant+%27y%27.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Use+of+undefined+constant+y+-+assumed+%27y%27+%28this+will+throw+an+Error+in+a+future+version+of+PHP%29.html>`_




Suggestions
___________

* Define the constant
* Turn the dynamic syntax into a normal variable syntax
* Use a fully qualified name (at least one \ ) to turn this syntax into a Fatal error when the constant is not found. This doesn't fix the problem, but may make it more obvious during the diagnostic.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/UndefinedConstantName                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


