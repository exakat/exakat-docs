.. _structures-dontusethetypeasvariable:

.. _don't-use-the-type-as-variable-name:

Don't Use The Type As Variable Name
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Don't Use The Type As Variable Name: When it is difficult to find a good name, it is very tempting to use the type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Use The Type As Variable Name
	:twitter:description: Don't Use The Type As Variable Name: When it is difficult to find a good name, it is very tempting to use the type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Use The Type As Variable Name
	:og:type: article
	:og:description: When it is difficult to find a good name, it is very tempting to use the type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Don't Use The Type As Variable Name.html
	:og:locale: en
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


