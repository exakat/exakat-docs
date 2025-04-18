.. _structures-usearrayfunctions:


.. _use-array-functions:

Use Array Functions
+++++++++++++++++++

.. meta::
	:description:
		Use Array Functions: There are a lot of native PHP functions for arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Array Functions
	:twitter:description: Use Array Functions: There are a lot of native PHP functions for arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Array Functions
	:og:type: article
	:og:description: There are a lot of native PHP functions for arrays
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Array Functions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseArrayFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseArrayFunctions.html","name":"Use Array Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"There are a lot of native PHP functions for arrays","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use Array Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There are a lot of native PHP functions for arrays. It is often faster to take advantage of them than write a loop.

* `array_push() <https://www.php.net/array_push>`_ : use `array_merge() <https://www.php.net/array_merge>`_
* `array_slice() <https://www.php.net/array_slice>`_ : use `array_chunk() <https://www.php.net/array_chunk>`_
* index access : use `array_column() <https://www.php.net/array_column>`_
* append `[]`: use `array_merge() <https://www.php.net/array_merge>`_
* addition : use `array_sum() <https://www.php.net/array_sum>`_
* multiplication : use `array_product() <https://www.php.net/array_product>`_
* concatenation : use `implode() <https://www.php.net/implode>`_
* ifthen : use `array_filter() <https://www.php.net/array_filter>`_
* extract one index $s['index'] : use `array_column() <https://www.php.net/array_column>`_
* apply a method to each element : use `array_map() <https://www.php.net/array_map>`_ or `array_walk() <https://www.php.net/array_walk>`_



.. code-block:: php
   
   <?php
   
   $all = implode('-', $s).'-';
   
   // same as above
   $all = '';
   foreach($array as $s) {
       $all .= $s . '-';
   }
   
   // extract one index in an array
   $extract = [];
   foreach($array as $a) {
   	$extract[] = $a['index'];
   }
   
   $extract = array_column($array, 'index');
   
   ?>

See also `Array Functions <https://www.php.net/manual/en/ref.array.php>`_ and :ref:`No array_merge() In Loops <no-array\_merge()-in-loops>`.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Remove the loop and use a native PHP function
* Add more expressions to the loop : batching multiple operations in one loop makes it more interesting than running separates loops.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseArrayFunctions                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


