.. _structures-dontusethetypeasvariable:

.. _dont-use-the-type-as-variable:

Dont Use The Type As Variable
+++++++++++++++++++++++++++++

  When it is difficult to find a good name, it is very tempting to use the type.

Such a name should carry its actual usage, as the type is already hold by the data.

This rule check for parameters and variables which uses the type as name. It also report instantiation which hold the same name than the instantiated class.

$`sqlite3 <https://www.php.net/sqlite3>`_ = new `Sqlite3() <https://www.php.net/sqlite3>`_;

function foo(int $int) : array {
	$array = [];
	return $array;
}

Suggestions
___________

* Use another name than the class or the type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontUseTheTypeAsVariable                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Semantics <ruleset-Semantics>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | semantics                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


