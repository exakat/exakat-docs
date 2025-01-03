.. _php-nostringwithappend:

.. _no-string-with-append:

No String With Append
+++++++++++++++++++++

.. meta::
	:description:
		No String With Append: PHP 7 doesn't allow the usage of [] with strings.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No String With Append
	:twitter:description: No String With Append: PHP 7 doesn't allow the usage of [] with strings
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No String With Append
	:og:type: article
	:og:description: PHP 7 doesn't allow the usage of [] with strings
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No String With Append.html
	:og:locale: en
PHP 7 doesn't allow the usage of [] with strings. [] is an array-only operator.



This was possible in PHP 5, but is now forbidden in PHP 7.

.. code-block:: php
   
   <?php
   
   $string = 'abc';
   
   // Not possible in PHP 7
   $string[] = 'd';
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.

Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_
  + `append <https://php-dictionary.readthedocs.io/en/latest/dictionary/append.ini.html>`_


Suggestions
___________

* Use the concatenation operator ``.`` to append strings.
* Use the concatenation short assignement ``.=`` to append strings.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoStringWithAppend                                                                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


