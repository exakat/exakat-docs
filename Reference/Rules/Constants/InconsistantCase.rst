.. _constants-inconsistantcase:

.. _true-false-inconsistant-case:

True False Inconsistant Case
++++++++++++++++++++++++++++

  `TRUE <https://www.php.net/TRUE>`_, true or True is the favorite way to write these values.

Usually, source code chooses either ALL CAPS booleans and null, either all lowercase. Sometimes, there is no standard.

When the source code uses a majority of one of the above convention, then the analyzer reports all remaining inconsistently cased constants.

This rule works on booleans and the null value, altogether.


.. code-block:: php
   
   <?php
   
   $a1 = true;
   $a2 = true;
   $a3 = true;
   $a4 = true;
   $a5 = true;
   $a6 = true;
   $a7 = true;
   $a8 = true;
   $a9 = true;
   $a10 = true;
   
   // This convention is inconsistence with the rest
   $b1 = TRUE;
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/InconsistantCase                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


