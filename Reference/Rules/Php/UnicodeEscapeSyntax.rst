.. _php-unicodeescapesyntax:

.. _unicode-escape-syntax:

Unicode Escape Syntax
+++++++++++++++++++++

.. meta::
	:description:
		Unicode Escape Syntax: Usage of the Unicode Escape syntax, with the ``\u{xxxxx}`` format, available since PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unicode Escape Syntax
	:twitter:description: Unicode Escape Syntax: Usage of the Unicode Escape syntax, with the ``\u{xxxxx}`` format, available since PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unicode Escape Syntax
	:og:type: article
	:og:description: Usage of the Unicode Escape syntax, with the ``\u{xxxxx}`` format, available since PHP 7
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/UnicodeEscapeSyntax.html
	:og:locale: en
Usage of the Unicode Escape syntax, with the ``\u{xxxxx}`` format, available since PHP 7.0.

.. code-block:: php
   
   <?php
   
   // Produce an elephant icon in PHP 7.0+
   echo "\u{1F418}";
   
   // Produce the raw sequence in PHP 5.0
   echo "\u{1F418}";
   
   ?>

See also `PHP RFC: Unicode Codepoint Escape Syntax <https://wiki.php.net/rfc/unicode_escape>`_, `Code point <https://en.wikipedia.org/wiki/Code_point>`_ and `Unicode <https://en.wikipedia.org/wiki/Unicode>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Invalid+UTF-8+codepoint+escape%3A+Codepoint+too+large.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Invalid+UTF-8+codepoint+escape+sequence.html>`_



Connex PHP features
-------------------

  + `unicode <https://php-dictionary.readthedocs.io/en/latest/dictionary/unicode.ini.html>`_
  + `escape-sequence <https://php-dictionary.readthedocs.io/en/latest/dictionary/escape-sequence.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UnicodeEscapeSyntax                                                                                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


