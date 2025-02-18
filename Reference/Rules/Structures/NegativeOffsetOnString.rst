.. _structures-negativeoffsetonstring:


.. _negative-offset-on-string:

Negative Offset On String
+++++++++++++++++++++++++

.. meta::
	:description:
		Negative Offset On String: Strings accept negative offset, when accessing one of the bytes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Negative Offset On String
	:twitter:description: Negative Offset On String: Strings accept negative offset, when accessing one of the bytes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Negative Offset On String
	:og:type: article
	:og:description: Strings accept negative offset, when accessing one of the bytes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Negative Offset On String.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NegativeOffsetOnString.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NegativeOffsetOnString.html","name":"Negative Offset On String","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 30 Jan 2025 17:07:33 +0000","dateModified":"Thu, 30 Jan 2025 17:07:33 +0000","description":"Strings accept negative offset, when accessing one of the bytes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Negative Offset On String.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Strings accept negative offset, when accessing one of the bytes. The negative offsets start from the end of the string, while the positive offsets start at the beginning.

-1 is the first character, as the end of the string; ``- strlen($string)`` is the first character: it is the length's character, starting from the last on. ``- strlen($string) - 1`` and later yield a warning about ``uninitialized string offset``.

Negative offsets are efficient to extract the end characters, compared to use ``substr()`` or ``count()``. They are not adapted to extract substrings.

This feature was added in PHP 7.1.

.. code-block:: php
   
   <?php
   
   $string = 'abcd';
   
   echo $string[1]; // b
   echo $string[-1]; // d
   echo $string[-4]; // a
   
   ?>
Related PHP errors 
-------------------

  + `Uninitialized string offset <https://php-errors.readthedocs.io/en/latest/messages/uninitialized-string-offset.html>`_



Connex PHP features
-------------------

  + `String <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_
  + `negative-index <https://php-dictionary.readthedocs.io/en/latest/dictionary/negative-index.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NegativeOffsetOnString                                                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.7.0                                                                                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.1 and more recent                                                                                                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


