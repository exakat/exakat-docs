.. _php-php80removeddirective:

.. _php-8.0-removed-directives:

PHP 8.0 Removed Directives
++++++++++++++++++++++++++

.. meta::
	:description:
		PHP 8.0 Removed Directives: List of directives that are removed in PHP 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP 8.0 Removed Directives
	:twitter:description: PHP 8.0 Removed Directives: List of directives that are removed in PHP 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP 8.0 Removed Directives
	:og:type: article
	:og:description: List of directives that are removed in PHP 8
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Php80RemovedDirective.html
	:og:locale: en
List of directives that are removed in PHP 8.0.

In PHP 8.0, `track_errors` was removed. 

You can detect valid directives with `ini_get() <https://www.php.net/ini_get>`_. This native function will return false, when the directive doesn't exist, while actual directive values will be returned as a string. 

See `Deprecation `track_errors <https://www.php.net/manual/en/errorfunc.configuration.php#ini.track-errors>`_ <https://www.php.net/manual/en/migration80.incompatible.php`_.

.. code-block:: php
   
   <?php
   
   var_dump(ini_get('track_errors'));
   
   ?>
Connex PHP features
-------------------

  + `directive <https://php-dictionary.readthedocs.io/en/latest/dictionary/directive.ini.html>`_


Suggestions
___________

* Remove usage of `track_errors`.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php80RemovedDirective                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`php-7.4-removed-directives`, :ref:`php-8.1-removed-directives`                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


