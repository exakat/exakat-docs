.. _structures-shoulduseoperator:


.. _should-use-operator:

Should Use Operator
+++++++++++++++++++

.. meta::
	:description:
		Should Use Operator: Some functions duplicate the feature of an operator.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Operator
	:twitter:description: Should Use Operator: Some functions duplicate the feature of an operator
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Operator
	:og:type: article
	:og:description: Some functions duplicate the feature of an operator
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use Operator.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShouldUseOperator.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShouldUseOperator.html","name":"Should Use Operator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"Some functions duplicate the feature of an operator","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Use Operator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Some functions duplicate the feature of an operator. When in doubt, it is better to use the operator. 

Beware, some edge cases may apply. In particular, backward compatibility may prevent usage of newer features.

* `array_push() <https://www.php.net/array_push>`_ is equivalent to [] 
* `is_object() <https://www.php.net/is_object>`_ is equivalent to `instanceof <https://www.php.net/manual/en/language.operators.type.php>`_
* function_get_arg() and function_get_args() is equivalent to ellipsis : `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_
* `chr() <https://www.php.net/chr>`_ is equivalent to string escape sequences, such as ``\n``, ``\x69``, ``u{04699}``
* `call_user_func() <https://www.php.net/call_user_func>`_ is equivalent to ``$functionName(arguments)``, ``$object->$method(`... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_$arguments)``
* `is_null() <https://www.php.net/is_null>`_ is equivalent to ``=== null``
* php_version() is equivalent to ``PHP_VERSION`` (the constant)
* `is_array() <https://www.php.net/is_array>`_, `is_int() <https://www.php.net/is_int>`_, `is_object() <https://www.php.net/is_object>`_, etc. is equivalent to a scalar type
Connex PHP features
-------------------

  + `operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/operator.ini.html>`_


Suggestions
___________

* Use [] instead of array_push()
* Use instanceof instead of is_object()
* Use ... instead of function_get_arg() and function_get_args()
* Use escape sequences instead of chr()
* Use dynamic function call instead of call_user_func()
* Use === null instead of is_null()
* Use PHP_VERSION instead of php_version()
* Use type instead of is_int(), is_string(), is_bool(), etc.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldUseOperator                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-structures-shoulduseoperator`, :ref:`case-sugarcrm-structures-shoulduseoperator`                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


