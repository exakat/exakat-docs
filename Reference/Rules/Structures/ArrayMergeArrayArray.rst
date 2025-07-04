.. _structures-arraymergearrayarray:


.. _array\_merge-needs-array-of-arrays:

Array_merge Needs Array Of Arrays
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Array_merge Needs Array Of Arrays: When collecting data to feed array_merge(), use an array of array as default value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Array_merge Needs Array Of Arrays
	:twitter:description: Array_merge Needs Array Of Arrays: When collecting data to feed array_merge(), use an array of array as default value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Array_merge Needs Array Of Arrays
	:og:type: article
	:og:description: When collecting data to feed array_merge(), use an array of array as default value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Array_merge Needs Array Of Arrays.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMergeArrayArray.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayMergeArrayArray.html","name":"Array_merge Needs Array Of Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When collecting data to feed array_merge(), use an array of array as default value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Array_merge Needs Array Of Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When collecting data to feed `array_merge() <https://www.php.net/array_merge>`_, use an array of array as default value. ```array(`array()) <https://www.php.net/array>`_``` is the neutral value for `array_merge() <https://www.php.net/array_merge>`_;

This analysis also reports when the used types are not an array : `array_merge() <https://www.php.net/array_merge>`_ does not accept scalar values, but only arrays.

Since PHP 7.4, it is possible to call `array_merge() <https://www.php.net/array_merge>`_ without an argument : this means the default value may an empty array. 

.. code-block:: php
   
   <?php
   
   // safe default value
   $a = array(array());
   
   // when $list is empty, this will trigger an error during array_merge()
   foreach($list as $l) {
       $a[] = $l;
   }
   $b = array_merge(...$a);
   
   ?>

See also `array_merge <https://www.php.net/array_merge>`_.

Connex PHP features
-------------------

  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use ```array(array())``` or ```[[]]``` as default value for array_merge()
* Remove any non-array value from the values in the default array




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMergeArrayArray                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


