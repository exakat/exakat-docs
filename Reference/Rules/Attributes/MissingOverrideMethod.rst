.. _attributes-missingoverridemethod:

.. _missing-overriden-method:

Missing Overriden Method
++++++++++++++++++++++++

  This rule reports methods which bears the `override <https://www.php.net/override>`_ `attribute <https://www.php.net/attribute>`_, but cannot have an eponymous method in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class.

This happens when the class has no `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, or when a trait is used in class without `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

As such, an `error <https://www.php.net/error>`_ will be raised when the class is used.

.. code-block:: php
   
   <?php
   
   
   ?>

Specs
_____

+--------------+----------------------------------+
| Short name   | Attributes/MissingOverrideMethod |
+--------------+----------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`         |
+--------------+----------------------------------+
| Exakat since | 2.6.8                            |
+--------------+----------------------------------+
| Severity     | Minor                            |
+--------------+----------------------------------+
| Time To Fix  | Quick (30 mins)                  |
+--------------+----------------------------------+
| Precision    | High                             |
+--------------+----------------------------------+
| Features     | override                         |
+--------------+----------------------------------+
| Available in |                                  |
+--------------+----------------------------------+


