.. _php-unicodeescapepartial:

.. _unicode-escape-partial:

Unicode Escape Partial
++++++++++++++++++++++

.. meta::
	:description:
		Unicode Escape Partial: PHP 7 introduces a new escape sequence for strings : \u{hex}.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unicode Escape Partial
	:twitter:description: Unicode Escape Partial: PHP 7 introduces a new escape sequence for strings : \u{hex}
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unicode Escape Partial
	:og:type: article
	:og:description: PHP 7 introduces a new escape sequence for strings : \u{hex}
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unicode Escape Partial.html
	:og:locale: en
PHP 7 introduces a new escape sequence for strings : \u{hex}. It is backward incompatible with previous PHP versions for two reasons : 

PHP 7 will recognize en replace those sequences, while PHP 5 keep them intact.
PHP 7 will halt on partial Unicode Sequences, as it tries to understand them, but may fail. 
Is is recommended to check all those strings, and make sure they will behave correctly in PHP 7.

.. code-block:: php
   
   <?php
   
   echo "\u{1F418}\n"; 
   // PHP 5 displays the same string
   // PHP 7 displays : an elephant
   
   echo "\u{NOT A UNICODE CODEPOINT}\n";
   // PHP 5 displays the same string
   // PHP 7 emits a fatal error
   
   ?>
Connex PHP features
-------------------

  + `unicode <https://php-dictionary.readthedocs.io/en/latest/dictionary/unicode.ini.html>`_
  + `escape-sequence <https://php-dictionary.readthedocs.io/en/latest/dictionary/escape-sequence.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UnicodeEscapePartial                                                                                                                                                                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


