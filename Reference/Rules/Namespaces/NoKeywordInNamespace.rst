.. _namespaces-nokeywordinnamespace:

.. _no-keyword-in-namespace:

No Keyword In Namespace
+++++++++++++++++++++++

.. meta::
	:description:
		No Keyword In Namespace: PHP keywords were not allowed in namespaces' names.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Keyword In Namespace
	:twitter:description: No Keyword In Namespace: PHP keywords were not allowed in namespaces' names
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Keyword In Namespace
	:og:type: article
	:og:description: PHP keywords were not allowed in namespaces' names
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Namespaces/NoKeywordInNamespace.html
	:og:locale: en
PHP keywords were not allowed in namespaces' names. As a whole, or as a part of the namespace. The syntax was relaxed in PHP 8.0. 

This rule is only useful to keep compatibility with previous versions. It leads to a compilation `error <https://www.php.net/error>`_. 

While some keywords are highly specific to PHP, such as ``endswitch`` or ``__halt_compiler``, others are more common such as empty(), `isset() <https://www.www.php.net/isset>`_, use, global, function...
Usage of PHP keyword was also relaxed for method' name.

.. code-block:: php
   
   <?php
   
   namespace if {}
   namespace endswitch {}
   
   namespace a\empty\b {}
   
   namespace end {}
   
   ?>

Suggestions
___________

* Avoid supporting older PHP versions while having keywords in the namespaces
* Change the namespaces to use other words than keywords




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/NoKeywordInNamespace                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.9                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`php7-relaxed-keyword`                                                                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


