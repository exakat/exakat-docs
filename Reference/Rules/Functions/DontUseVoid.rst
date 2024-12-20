.. _functions-dontusevoid:

.. _don't-collect-void:

Don't Collect Void
++++++++++++++++++

  When a method has the return type void, there is no need to collect the `result <https://www.php.net/result>`_. The collected value is always ``null``.

With a ``void`` return type, the method is intented to be without return value. This analysis also include methods which are not returning anything, and could be completed with a ``void`` returntype.

.. code-block:: php
   
   <?php
   
   function foo() : void {
       // doSomething()
   }
   
   // This is useless
   $result = foo(); 
   
   // This is useless. It looks like this is a left over from code refactoring
   echo foo(); 
   
   // No explicitly returned values
   function goo() {
       // doSomething()
   }
   
   ?>
Connex PHP features
-------------------

  + `void <https://php-dictionary.readthedocs.io/en/latest/dictionary/void.ini.html>`_


Suggestions
___________

* Move the call to the function to its own expression with a semi-colon.
* Remove assignations of the result of these methods calls.
* Do not use these methods as parameters.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/DontUseVoid                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.9                                                                                                                   |
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


