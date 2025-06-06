.. _structures-regexdelimiter:


.. _regex-delimiter:

Regex Delimiter
+++++++++++++++

.. meta::
	:description:
		Regex Delimiter: PCRE regular expressions may use a variety of delimiters.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Regex Delimiter
	:twitter:description: Regex Delimiter: PCRE regular expressions may use a variety of delimiters
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Regex Delimiter
	:og:type: article
	:og:description: PCRE regular expressions may use a variety of delimiters
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Regex Delimiter.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RegexDelimiter.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RegexDelimiter.html","name":"Regex Delimiter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PCRE regular expressions may use a variety of delimiters","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Regex Delimiter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PCRE regular expressions may use a variety of delimiters. 

There seems to be a standard delimiter in the code, and some exceptions : one or several forms are dominant (> 90%), while the others are rare. 

The analyzed code has less than 10% of the rare delimiters. For consistency reasons, it is recommended to make them all the same. 

Generally, one or two delimiters are used, depending on the expected special chars in the scanned strings : for example, / tends to be avoided when parsing HTML.

Regex are literals, or partial literals, used in `preg_match() <https://www.php.net/preg_match>`_, `preg_match_all() <https://www.php.net/preg_match_all>`_, `preg_replace() <https://www.php.net/preg_replace>`_, `preg_replace_callback() <https://www.php.net/preg_replace_callback>`_, `preg_replace_callback_array() <https://www.php.net/preg_replace_callback_array>`_.

.. code-block:: php
   
   <?php
   
   echo 'a';
   echo 'b';
   echo 'c';
   echo 'd';
   echo 'e';
   echo 'f';
   echo 'g';
   echo 'h';
   echo 'i';
   echo 'j';
   echo 'k';
   
   // This should probably be written 'echo';
   print 'l';
   
   ?>

See also `Ideal regex delimiters in PHP <http://codelegance.com/ideal-regex-delimiters-in-php/>`_.

Connex PHP features
-------------------

  + `Regular Expressions <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RegexDelimiter                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


