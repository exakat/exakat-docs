.. _php-arraykeyexistswithobjects:


.. _array\_key\_exists()-works-on-arrays:

array_key_exists() Works On Arrays
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		array_key_exists() Works On Arrays: array_key_exists() requires arrays as second argument.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: array_key_exists() Works On Arrays
	:twitter:description: array_key_exists() Works On Arrays: array_key_exists() requires arrays as second argument
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: array_key_exists() Works On Arrays
	:og:type: article
	:og:description: array_key_exists() requires arrays as second argument
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/array_key_exists() Works On Arrays.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ArrayKeyExistsWithObjects.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ArrayKeyExistsWithObjects.html","name":"array_key_exists() Works On Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"array_key_exists() requires arrays as second argument","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/array_key_exists() Works On Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`array_key_exists() <https://www.php.net/array_key_exists>`_ requires arrays as second argument. Until PHP 7.4, objects were also allowed, yet it is now deprecated.

.. code-block:: php
   
   <?php
   
   // Valid way to check for key
   $array = ['a' => 1];
   var_dump(array_key_exists('a', $array))
   
   // Deprecated since PHP 7.4
   $object = new Stdclass();
   $object->a = 1;
   var_dump(array_key_exists('a', $object))
   
   ?>

See also `array_key_exists() with objects <https://wiki.php.net/rfc/deprecations_php_7_4#array_key_exists_with_objects>`_ and `array_key_exists <https://php.net/array-key-exists>`_.

Related PHP errors 
-------------------

  + `Using array_key_exists() on objects is deprecated. Use isset() or property_exists() instead <https://php-errors.readthedocs.io/en/latest/messages/using-array_key_exists%28%29-on-objects-is-deprecated..html>`_



Connex PHP features
-------------------

  + `Index <https://php-dictionary.readthedocs.io/en/latest/dictionary/index.ini.html>`_
  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use the (array) cast to turn the object into an array
* Use the native PHP function proprety_exists() or isset() on the property to check them.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ArrayKeyExistsWithObjects                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


