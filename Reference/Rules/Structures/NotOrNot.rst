.. _structures-notornot:

.. _not-or-tilde:

Not Or Tilde
++++++++++++

  There are two NOT operator in PHP : ``!`` and ``~``. The first is a logical operator, and returns a boolean. The second is a bit-wise operator, and flips each bit. 

Although they are distinct operations, there are situations where they provide the same results. In particular, when processing booleans. 

Yet, ``!`` and ``~`` are not the same. ``~`` has a higher priority, and will not yield to ``instanceof``, while ``!`` does.

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   // be consistent
   if (!$condition) {
       doSomething();
   }
   
   if (~$condition) {
       doSomething();
   }
   
   ?>

See also `Bitwise Operators <https://www.php.net/manual/en/language.operators.bitwise.php>`_, `Logical Operators <https://www.php.net/manual/en/language.operators.logical.php>`_ and `Operators Precedences <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `logical-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/logical-operator.ini.html>`_
  + `bitwise-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/bitwise-operator.ini.html>`_


Suggestions
___________

* Use the ! in logical expressions
* Use the ~ in bitwise expressions, with integers for example




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NotOrNot                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.9                                                                                                                   |
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


