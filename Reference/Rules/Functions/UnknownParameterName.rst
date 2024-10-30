.. _functions-unknownparametername:

.. _unknown-parameter-name:

Unknown Parameter Name
++++++++++++++++++++++

  The name of the parameter doesn't belong to the method signature. Named arguments were introduced in PHP 8.0.

Named arguments errors will also arise when spreading a hash array with arbitrary number of arguments. For example, with `array_merge() <https://www.php.net/array_merge>`_, the array should not use named keys.

.. code-block:: php
   
   <?php
   
   // All good
   foo(a:1, b:2, c:3);
   foo(...['a':1, 'b':2, 'c':3]);
   
   // A is not a parameter name, it should be a : names are case sensitive
   foo(A:1, b:2, c:3);
   foo(...['A':1, 'b':2, 'c':3]);
   
   function foo($a, $b, $c) {}
   
   array_merge(['a' => [1], 'b' => [2]]);
   ?>

See also `Named Arguments <https://wiki.php.net/rfc/named_params>`_ and :ref:`Wrong Argument Name With PHP Function <wrong-argument-name-with-php-function>`.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Unknown+named+parameter+%24d+in.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/array_merge%28%29+does+not+accept+unknown+named+parameters.html>`_



Connex PHP features
-------------------

  + `named-parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameter.ini.html>`_


Suggestions
___________

* Fix the name of the parameter and use a valid one
* Remove the parameter name, and revert to positional notation




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnknownParameterName                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


