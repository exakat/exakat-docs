.. _arrays-ambiguouskeys:


.. _ambiguous-array-index:

Ambiguous Array Index
+++++++++++++++++++++

.. meta::
	:description:
		Ambiguous Array Index: Indexes should not be defined with different types than int or string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Ambiguous Array Index
	:twitter:description: Ambiguous Array Index: Indexes should not be defined with different types than int or string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Ambiguous Array Index
	:og:type: article
	:og:description: Indexes should not be defined with different types than int or string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Ambiguous Array Index.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/AmbiguousKeys.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/AmbiguousKeys.html","name":"Ambiguous Array Index","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Indexes should not be defined with different types than int or string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Ambiguous Array Index.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Indexes should not be defined with different types than int or string. 

Array indices only accept integers and strings, so any other type of literal is reported. In fact, ``null`` is turned into an empty string, booleans are turned into an integer, and real numbers are truncated (not rounded).

They are indeed distinct, but may lead to confusion.

.. code-block:: php
   
   <?php
   
   $x = [ 1  => 1,
         '1' => 2,
         1.0 => 3,
         true => 4];
   // $x only contains one element : 1 => 4
   
   // Still wrong, immediate typecast to 1
   $x[1.0]  = 5; 
   $x[true] = 6; 
   
   ?>

See also `array <https://www.php.net/manual/en/language.types.array.php>`_.

Connex PHP features
-------------------

  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Only use string or integer as key for an array. 
* Use transtyping operator (string) and (int) to make sure of the type




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/AmbiguousKeys                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-prestashop-arrays-ambiguouskeys`, :ref:`case-mautic-arrays-ambiguouskeys`                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


