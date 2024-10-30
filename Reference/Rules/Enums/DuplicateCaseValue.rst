.. _enums-duplicatecasevalue:

.. _duplicate-enum-case-value:

Duplicate Enum Case Value
+++++++++++++++++++++++++

  In a backed enumeration, may it be ``int`` or ``string``, the values of the cases must all be distinct. There can't be two of them of the same value.

.. code-block:: php
   
   <?php
   
   enum e: int {
   	case A = 1 + 1;
   	case B = 2;
   }
   
   enum e2: string {
   	case A = 'A';
   	case B = 'A';
   }
   
   ?>
Connex PHP features
-------------------

  + `hook <https://php-dictionary.readthedocs.io/en/latest/dictionary/hook.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------+
| Short name   | Enums/DuplicateCaseValue                                   |
+--------------+------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>` |
+--------------+------------------------------------------------------------+
| Exakat since | 2.6.8                                                      |
+--------------+------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                               |
+--------------+------------------------------------------------------------+
| Severity     | Minor                                                      |
+--------------+------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                            |
+--------------+------------------------------------------------------------+
| Precision    | Very high                                                  |
+--------------+------------------------------------------------------------+
| Available in |                                                            |
+--------------+------------------------------------------------------------+


