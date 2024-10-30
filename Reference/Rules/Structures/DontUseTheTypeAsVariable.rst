.. _structures-dontusethetypeasvariable:

.. _don't-use-the-type-as-variable-name:

Don't Use The Type As Variable Name
+++++++++++++++++++++++++++++++++++

  When it is difficult to find a good name, it is very tempting to use the type.

Such a name should carry its actual usage, as the type is already hold by the data.

This rule check for parameters and variables which uses the type as name. It also report instantiation which hold the same name than the instantiated class.

.. code-block:: php
   
   <?php
   
   $sqlite3 = new Sqlite3();
   
   function foo(int $int) : array {
   	$array = [];
   	return $array;
   }
   ?>
Connex PHP features
-------------------

  + `semantics <https://php-dictionary.readthedocs.io/en/latest/dictionary/semantics.ini.html>`_


Suggestions
___________

* Use another name than the class or the type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontUseTheTypeAsVariable                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


