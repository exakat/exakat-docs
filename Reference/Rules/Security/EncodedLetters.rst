.. _security-encodedletters:

.. _encoded-simple-letters:

Encoded Simple Letters
++++++++++++++++++++++

.. meta::
	:description:
		Encoded Simple Letters: Some simple letters are written in escape sequence.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Encoded Simple Letters
	:twitter:description: Encoded Simple Letters: Some simple letters are written in escape sequence
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Encoded Simple Letters
	:og:type: article
	:og:description: Some simple letters are written in escape sequence
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Security/EncodedLetters.html
	:og:locale: en
Some simple letters are written in escape sequence. 

Usually, escape sequences are made to encode unusual characters. Using escape sequences for simple characters, like letters or numbers is suspicious.

This analysis also detects Unicode codepoint with superfluous leading zeros.

.. code-block:: php
   
   <?php
   
   // This escape sequence makes eval hard to spot
   $a = "ev\101l";
   $a('php_info();');
   
   // With a PHP 7.0 unicode code point sequence
   $a = "ev\u{000041}l";
   $a('php_info();');
   
   // With a PHP 5.0+ hexadecimal sequence
   $a = "ev\x41l";
   $a('php_info();');
   
   ?>
Connex PHP features
-------------------

  + `string-sequence <https://php-dictionary.readthedocs.io/en/latest/dictionary/string-sequence.ini.html>`_


Suggestions
___________

* Make all simple letter appear clearly
* Add comments about why this code is encoded




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/EncodedLetters                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-security-encodedletters`                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


