.. _structures-arraymappassesbyvalue:


.. _array\_map()-passes-by-value:

Array_Map() Passes By Value
+++++++++++++++++++++++++++

.. meta::
	:description:
		Array_Map() Passes By Value: array_map() requires the callback to receive elements by value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Array_Map() Passes By Value
	:twitter:description: Array_Map() Passes By Value: array_map() requires the callback to receive elements by value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Array_Map() Passes By Value
	:og:type: article
	:og:description: array_map() requires the callback to receive elements by value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Array_Map() Passes By Value.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMapPassesByValue.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMapPassesByValue.html","name":"Array_Map() Passes By Value","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"array_map() requires the callback to receive elements by value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Array_Map() Passes By Value.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`array_map() <https://www.php.net/array_map>`_ requires the callback to receive elements by value. Unlike `array_walk() <https://www.php.net/array_walk>`_, which accepts by value or by reference, depending on the action taken.

PHP 8.0 and more recent emits a Warning

.. code-block:: php
   
   <?php
   // Example, courtery of Juliette Reinders Folmer
   function trimNewlines(&$line, $key) {
       $line = str_replace(array("\n", "\r" ), '', $line);
   }
   
   $original = [
       "text\n\n",
       "text\n\r" 
   ];
   
   $array = $original;
   array_walk($array, 'trimNewlines');
   
   var_dump($array);
   
   array_map('trimNewlines', $original, [0, 1]);
   
   ?>

See also `array_map <https://www.php.net/array_map>`_.

Related PHP errors 
-------------------

  + `Argument #1 ($line) must be passed by reference <https://php-errors.readthedocs.io/en/latest/messages/%25s%25s%25s%28%29%3A-argument-%23%25d%25s%25s%25s-must-be-passed-by-reference%2C-value-given.html>`_



Connex PHP features
-------------------

  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `Map <https://php-dictionary.readthedocs.io/en/latest/dictionary/map.ini.html>`_
  + `Passing By Value <https://php-dictionary.readthedocs.io/en/latest/dictionary/by-value.ini.html>`_
  + `Passing By Reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/by-reference.ini.html>`_


Suggestions
___________

* Make the callback first argument a reference




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMapPassesByValue                                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


