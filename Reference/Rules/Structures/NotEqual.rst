.. _structures-notequal:

.. _not-equal-is-not-!==:

Not Equal Is Not !==
++++++++++++++++++++

  Not and Equal operators, used separately, don't amount to the different operator ``!==``.

``!$a == $b`` first turns ``$a``into the opposite boolean, then compares this boolean value to ``$b``. On the other hand, ``$a !== $b`` compares the two variables for type and value, and returns a boolean. 
Note that the ``instanceof`` operator may be use with this syntax, due to operator precedence.

.. code-block:: php
   
   <?php
   
   if ($string != 'abc') {
       // doSomething()
   }
   
   // Here, string will be an boolean, leading 
   if (!$string == 'abc') {
       // doSomething()
   }
   
   // operator priority may be confusing
   if (!$object instanceof OneClass) {
       // doSomething()
   }
   ?>

See also `Operator Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Suggestions
___________

* Use the != or !==
* Use parenthesis




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NotEqual                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


