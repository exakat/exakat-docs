.. _classes-magicmethodreturntypes:

.. _magic-method-returntype-is-restricted:

Magic Method Returntype Is Restricted
+++++++++++++++++++++++++++++++++++++

  Some magic method have compulsory return types. 

+ `__destruct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ : ``void``
+ `__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ : ``void``
+ __unserialize() : ``void``
+ `__unset() <https://www.php.net/manual/en/language.oop5.magic.php>`_ : ``void``
+ `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_ : ``void``
+ __serialize() : ``array``
+ `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_ : ``bool``
+ `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ : ``string``

The others may use mixed, or a more restrictive one.

See also `Magic Methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.


Suggestions
___________

* Use the right return type for the magic method
* Do not use any return type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MagicMethodReturntypes                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


