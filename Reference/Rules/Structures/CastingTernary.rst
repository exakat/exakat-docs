.. _structures-castingternary:

.. _casting-ternary:

Casting Ternary
+++++++++++++++

  Type casting has a precedence over ternary operator, and is applied first. When this happens, the condition is cast, although it is often useless as PHP will do it if needed.

This applies to the ternary operator, the coalesce operator ?: and the null-coalesce operator ??.
The last example generates first an `error <https://www.php.net/error>`_ `Undefined variable: b`, since $b is first cast to a string. The `result <https://www.php.net/result>`_ is then an empty string, which leads to an empty string to be stored into $a. Multiple errors cascade.

.. code-block:: php
   
   <?php
       $a = (string) $b ? 3 : 4;
       $a = (string) $b ?: 4;
       $a = (string) $b ?? 4;
   ?>

See also `Operators Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Related PHP errors 
-------------------

  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Undefined+variable%3A.html>`_



Connex PHP features
-------------------

  + `ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_
  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Add parenthesis around the ternary operator
* Skip the casting
* Cast in another expression




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CastingTernary                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


