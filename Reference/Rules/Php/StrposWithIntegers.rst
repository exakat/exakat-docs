.. _php-strposwithintegers:


.. _strpos()-with-integers:

strpos() With Integers
++++++++++++++++++++++

.. meta::
	:description:
		strpos() With Integers: strpos() used to accept integer as second argument, and turn them into their ASCII equivalent.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: strpos() With Integers
	:twitter:description: strpos() With Integers: strpos() used to accept integer as second argument, and turn them into their ASCII equivalent
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: strpos() With Integers
	:og:type: article
	:og:description: strpos() used to accept integer as second argument, and turn them into their ASCII equivalent
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/strpos() With Integers.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/StrposWithIntegers.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/StrposWithIntegers.html","name":"strpos() With Integers","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"strpos() used to accept integer as second argument, and turn them into their ASCII equivalent","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/strpos() With Integers.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`strpos() <https://www.php.net/strpos>`_ used to accept integer as second argument, and turn them into their ASCII equivalent. This was deprecated in PHP 7.x, and dropped in 8.0.

It is recommended to use casting to ensure the variable is actually strings, and `strpos() <https://www.php.net/strpos>`_ behaves as expected.

.. code-block:: php
   
   <?php
   
   strpos('abc ', 32);
   // PHP 8.0+ : false, 32 is not found
   // PHP 7.4- : 3, 32 is turned into space, then found
   
   ?>
Related PHP errors 
-------------------

  + `needle is not a string or an integer <https://php-errors.readthedocs.io/en/latest/messages/needle-is-not-a-string-or-an-integer.html>`_
  + `Non-string needles will be interpreted as strings in the future. Use an explicit chr() call to preserve the current behavior <https://php-errors.readthedocs.io/en/latest/messages/non-string-needles-will-be-interpreted-as-strings-in-the-future.-use-an-explicit-chr%28%29-call-to-preserve-the-current-behavior.html>`_



Connex PHP features
-------------------

  + `Arcane <https://php-dictionary.readthedocs.io/en/latest/dictionary/arcane.ini.html>`_


Suggestions
___________

* Add a cast to make the data string
* Test the data to be a string before usage




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/StrposWithIntegers                                                                                                  |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.5.2                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and more recent                                                                                            |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/strposWithInteger.html>`__             |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                    |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


