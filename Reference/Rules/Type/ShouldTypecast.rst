.. _type-shouldtypecast:

.. _should-typecast:

Should Typecast
+++++++++++++++

  When typecasting, it is better to use the casting operator, such as ``(int)`` or ``(bool)``.

Functions such as `intval() <https://www.php.net/intval>`_ or `settype() <https://www.php.net/settype>`_ are always slower.
This is a micro-optimisation, although such conversion may be use multiple times, leading to a larger performance increase.  

Note that `intval() <https://www.php.net/intval>`_ may also be used to convert an integer to another base. `Intval() <https://www.php.net/intval>`_ called with 2 arguments are skipped by this rule.

.. code-block:: php
   
   <?php
   
   // Fast version
   $int = (int) $X;
   
   // Slow version
   $int = intval($X);
   
   // Convert to base 8 : can't use (int) for that
   $int = intval($X, 8);
   
   
   ?>
Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Use a typecast, instead of a functioncall.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/ShouldTypecast                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Rector <ruleset-Rector>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-type-shouldtypecast`, :ref:`case-openconf-type-shouldtypecast`                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


