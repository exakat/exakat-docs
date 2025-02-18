.. _structures-onlyfirstbyte:


.. _only-first-byte-will-be-assigned:

Only First Byte Will Be Assigned
++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Only First Byte Will Be Assigned: When assigning a string to a string with the array syntax, only the first byte is used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Only First Byte Will Be Assigned
	:twitter:description: Only First Byte Will Be Assigned: When assigning a string to a string with the array syntax, only the first byte is used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Only First Byte Will Be Assigned
	:og:type: article
	:og:description: When assigning a string to a string with the array syntax, only the first byte is used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Only First Byte Will Be Assigned.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OnlyFirstByte.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OnlyFirstByte.html","name":"Only First Byte Will Be Assigned","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 11 Feb 2025 09:13:38 +0000","dateModified":"Tue, 11 Feb 2025 09:13:38 +0000","description":"When assigning a string to a string with the array syntax, only the first byte is used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Only First Byte Will Be Assigned.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When assigning a string to a string with the array syntax, only the first byte is used. This is because the offset locates a single byte. 

In ASCII, that byte is also a character, and the `error <https://www.php.net/error>`_ message uses this fact.

.. code-block:: php
   
   <?php
   
   $str = 'xy';  
   
   // first letter is now a
   $str[0] = 'a';
   
   // second letter is now b, c is ignored
   $str[1] = 'bc';
   
   ?>

See also `String access and modification by character <https://www.php.net/manual/en/language.types.string.php#language.types.string.substr>`_.

Related PHP errors 
-------------------

  + `Only the first byte will be assigned to the string offset <https://php-errors.readthedocs.io/en/latest/messages/only-the-first-byte-will-be-assigned-to-the-string-offset.html>`_



Connex PHP features
-------------------

  + `Byte <https://php-dictionary.readthedocs.io/en/latest/dictionary/byte.ini.html>`_
  + `Character <https://php-dictionary.readthedocs.io/en/latest/dictionary/character.ini.html>`_
  + `String <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_
  + `Array Syntax <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-notation.ini.html>`_


Suggestions
___________

* Remove extra bytes when assigning to a string
* Use concatenation
* Use strpos() and substr() functions
* Use explode(), implode() functions and array manipulations




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/OnlyFirstByte                                                                                                |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.2                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0                                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                    |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


