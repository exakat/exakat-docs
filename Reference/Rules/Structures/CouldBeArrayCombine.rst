.. _structures-couldbearraycombine:


.. _could-be-array\_combine():

Could Be array_combine()
++++++++++++++++++++++++

.. meta::
	:description:
		Could Be array_combine(): This rule suggests using the native function array_combine() to merge two arrays into a hash.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be array_combine()
	:twitter:description: Could Be array_combine(): This rule suggests using the native function array_combine() to merge two arrays into a hash
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be array_combine()
	:og:type: article
	:og:description: This rule suggests using the native function array_combine() to merge two arrays into a hash
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be array_combine().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldBeArrayCombine.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldBeArrayCombine.html","name":"Could Be array_combine()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This rule suggests using the native function array_combine() to merge two arrays into a hash","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be array_combine().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule suggests using the native function `array_combine() <https://www.php.net/array_combine>`_ to merge two arrays into a hash. `array_combine() <https://www.php.net/array_combine>`_ takes the keys and the values from two distinct arrays, and merge them into one.

.. code-block:: php
   
   <?php
   
   $keys = [1, 2, 3];
   $values = ['a', 'b', 'c'];
   $destination = [];
   foreach($keys as $k => $v) {
   	$destination[$v] = $values[$k];
   }
   
   $destination = [1 => 'a', 2 => 'b', 3 => 'c'];
   
   $destination = array_combine($keys, $values);
   
   ?>

See also `How to use array_merge() and array_combine() in PHP ? <https://www.geeksforgeeks.org/how-to-use-array_merge-and-array_combine-in-php/>`_.

Connex PHP features
-------------------

  + `Hash <https://php-dictionary.readthedocs.io/en/latest/dictionary/hash.ini.html>`_


Suggestions
___________

* Use array_combine().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldBeArrayCombine                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


