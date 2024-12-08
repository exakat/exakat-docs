.. _functions-wrongargumenttype:

.. _wrong-argument-type:

Wrong Argument Type
+++++++++++++++++++

  Checks that the type of the argument is consistent with the type of the called method.
This analysis is valid with PHP 8.0.

.. code-block:: php
   
   <?php
   
   function foo(int $a) { }
   
   //valid call, with an integer
   foo(1);
   
   //invalid call, with a string
   foo('asd');
   
   ?>
Related PHP errors 
-------------------

  + `Argument #1 ($s) must be of type array, int given <https://php-errors.readthedocs.io/en/latest/messages/Argument+%23%25d+%28%24%25s%29+must+be+of+type+%25s%2C+%25s+given.html>`_



Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/argument.ini.html>`_


Suggestions
___________

* Always use a valid type when calling methods.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongArgumentType                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.3                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


