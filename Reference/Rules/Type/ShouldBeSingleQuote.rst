.. _type-shouldbesinglequote:


.. _should-be-single-quote:

Should Be Single Quote
++++++++++++++++++++++


.. meta::

	:description:

		Should Be Single Quote: Use single quote for simple strings.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Should Be Single Quote

	:twitter:description: Should Be Single Quote: Use single quote for simple strings

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Should Be Single Quote

	:og:type: article

	:og:description: Use single quote for simple strings

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Be Single Quote.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/ShouldBeSingleQuote.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/ShouldBeSingleQuote.html","name":"Should Be Single Quote","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use single quote for simple strings","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Be Single Quote.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use single quote for simple strings.

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ content inside a string, that has no single quotes nor escape sequence (such as \n or \t), should be using single quote delimiter, instead of double quote. 
If you have too many of them, don't loose your time switching them all. If you have a few of them, it may be good for consistence.

.. code-block:: php
   
   <?php
   
   $a = "abc";
   
   // This one is using a special sequence
   $b = "cde\n";
   
   // This one is using two special sequences
   $b = "\x03\u{1F418}";
   
   ?>
Connex PHP features
-------------------

  + `double-quote <https://php-dictionary.readthedocs.io/en/latest/dictionary/double-quote.ini.html>`_
  + `single-quote <https://php-dictionary.readthedocs.io/en/latest/dictionary/single-quote.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/ShouldBeSingleQuote                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-double-quote <https://github.com/dseguy/clearPHP/tree/master/rules/no-double-quote.md>`__                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


