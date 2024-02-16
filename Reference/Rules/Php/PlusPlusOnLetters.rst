.. _php-plusplusonletters:

.. _plus-plus-used-on-strings:

Plus Plus Used On Strings
+++++++++++++++++++++++++

  Reports strings that are incremented with the post increment operator ``'s'++``.

This spots issues of the famous feature of PHP : incrementing strings with letters.

This analysis checks for string to be incremented. It doesn't check if the string is a numeric string, but does check the type, implicit or explicit.

.. code-block:: php
   
   <?php
   
   $a = 'a';
   $a++;
   print $a;
   // prints b
   ?>

See also `Incrementing/Decrementing Operators <https://www.php.net/manual/en/language.operators.increment.php>`_ and `Path to Saner Increment/Decrement operators <https://wiki.php.net/rfc/saner-inc-dec-operators>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PlusPlusOnLetters                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


