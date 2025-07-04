.. _structures-arraywithstringellipsis:


.. _array-with-string-ellipsis:

Array With String Ellipsis
++++++++++++++++++++++++++

.. meta::
	:description:
		Array With String Ellipsis: In PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Array With String Ellipsis
	:twitter:description: Array With String Ellipsis: In PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Array With String Ellipsis
	:og:type: article
	:og:description: In PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Array With String Ellipsis.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayWithStringEllipsis.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayWithStringEllipsis.html","name":"Array With String Ellipsis","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"In PHP 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Array With String Ellipsis.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

In PHP 7.4, it was not possible to use the ``...`` spread operator with arrays that used string keys, as named parameters were not yet implemented.

.. code-block:: php
   
   <?php
   
   function foo($a, $b) {
       echo $a;
   }
   
   // This is not possible
   foo(...['a' => 1, 'b' => 2]);
   
   // This is possible
   foo(...[1, 2]);
   foo(...array_values([1, 2]));
   foo(...[3 => 1, 0 => 2]);
   
   ?>
Related PHP errors 
-------------------

  + `Cannot unpack array with string keys <https://php-errors.readthedocs.io/en/latest/messages/cannot-unpack-array-with-string-keys.html>`_



Connex PHP features
-------------------

  + `spread-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/spread-operator.ini.html>`_
  + `named-parameters <https://php-dictionary.readthedocs.io/en/latest/dictionary/named-parameters.ini.html>`_


Suggestions
___________

* Use ``array_keys()`` on the array before the spread, to ensure it only has integer index.
* Upgrade to PHP 8.0 or later.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/ArrayWithStringEllipsis                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>`, :ref:`CompatibilityPHP83 <ruleset-CompatibilityPHP83>`, :ref:`CompatibilityPHP84 <ruleset-CompatibilityPHP84>`, :ref:`CompatibilityPHP85 <ruleset-CompatibilityPHP85>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.7.0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.4 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/unpack_arrays_with_strings.html>`__                                                                                                                                                                                                                                                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Unknown                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


