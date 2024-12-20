.. _functions-wrongtypewithcall:

.. _wrong-type-with-call:

Wrong Type With Call
++++++++++++++++++++

  This analysis checks that a call to a method uses the types.

This analysis is compatible with Union types and with Intersection types.
Currently, this analysis doesn't take into account ``strict_types = 1``. As such, ``int`` and ``string`` won't be compatible.

.. code-block:: php
   
   <?php
   
   function foo(string $a) {
   
   }
   
   // wrong type used
   foo(1);
   
   // wrong type used
   foo("1");
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Argument+%231+%28%24s%29+must+be+of+type+X%2C+int+given.html>`_



Connex PHP features
-------------------

  + `union-type <https://php-dictionary.readthedocs.io/en/latest/dictionary/union-type.ini.html>`_
  + `intersection-type <https://php-dictionary.readthedocs.io/en/latest/dictionary/intersection-type.ini.html>`_


Suggestions
___________

* Use the right type with all arguments
* Force the type with a cast
* Check the type before calling




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongTypeWithCall                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


