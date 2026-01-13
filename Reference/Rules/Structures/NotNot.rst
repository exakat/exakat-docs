.. _structures-notnot:

.. _not-not:

Not Not
+++++++

  Double not makes a boolean, not a ``true``.

This is a wrong casting to boolean. PHP supports ``(boolean)`` to do the same, faster and cleaner.

.. code-block:: php
   
   <?php
       // Explicit code
       $b = (boolean) $x; 
       $b = (bool) $x; 
   
       // Wrong type casting
       $b = !!$x; 
   
   ?>

See also `Logical Operators <https://www.php.net/manual/en/language.operators.logical.php>`_ and `Type Juggling <https://www.php.net/manual/en/language.types.type-juggling.php>`_.

Connex PHP features
-------------------

  + `logical-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/logical-operator.ini.html>`_
  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Use ``(bool)`` casting operator for that
* Don't typecast, and let PHP handle it. This works in situations where the boolean is immediately used.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NotNot                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-implied-cast <https://github.com/dseguy/clearPHP/tree/master/rules/no-implied-cast.md>`__                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-cleverstyle-structures-notnot`, :ref:`case-tine20-structures-notnot`                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


