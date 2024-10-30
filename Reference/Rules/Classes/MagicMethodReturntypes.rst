.. _classes-magicmethodreturntypes:

.. _magic-method-returntype-is-restricted:

Magic Method Returntype Is Restricted
+++++++++++++++++++++++++++++++++++++

  Some PHP magic method have compulsory return types. This means that the type is compulsory, and it is applied by default, even if it is explicitely omitted. On the other hand, any other type is forbidden, and reported as such by PHP. 

+ `__destruct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ : ``void``
+ `__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ : ``void``
+ __unserialize() : ``void``
+ `__unset() <https://www.php.net/manual/en/language.oop5.magic.php>`_ : ``void``
+ `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_ : ``void``
+ __serialize() : ``array``
+ `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_ : ``bool``
+ `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ : ``string``

The others magic methods may use mixed, or a more restrictive type.

See also `Magic Methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Return+type+must+be+array+when+declared+in.html>`_



Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Use the right return type for the magic method
* Do not use any return type




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MagicMethodReturntypes                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `<?php                                                                                                                                                             |
|              |                                                                                                                                                                    |
|              | class x {                                                                                                                                                          |
|              | 	function __toString() : string {                                                                                                                                  |
|              | 		return 'string';                                                                                                                                                 |
|              | 	}                                                                                                                                                                 |
|              | }                                                                                                                                                                  |
|              |                                                                                                                                                                    |
|              | ?> <https://github.com/dseguy/clearPHP/tree/master/rules/<?php                                                                                                     |
|              |                                                                                                                                                                    |
|              | class x {                                                                                                                                                          |
|              | 	function __toString() : string {                                                                                                                                  |
|              | 		return 'string';                                                                                                                                                 |
|              | 	}                                                                                                                                                                 |
|              | }                                                                                                                                                                  |
|              |                                                                                                                                                                    |
|              | ?>.md>`__                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


