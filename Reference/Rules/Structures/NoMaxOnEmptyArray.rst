.. _structures-nomaxonemptyarray:


.. _no-max-on-empty-array:

No Max On Empty Array
+++++++++++++++++++++

.. meta::
	:description:
		No Max On Empty Array: Using max() or min() on an empty array leads to a ``valueError`` exception.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Max On Empty Array
	:twitter:description: No Max On Empty Array: Using max() or min() on an empty array leads to a ``valueError`` exception
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Max On Empty Array
	:og:type: article
	:og:description: Using max() or min() on an empty array leads to a ``valueError`` exception
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Max On Empty Array.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoMaxOnEmptyArray.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoMaxOnEmptyArray.html","name":"No Max On Empty Array","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"Using max() or min() on an empty array leads to a ``valueError`` exception","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Max On Empty Array.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Using `max() <https://www.php.net/max>`_ or `min() <https://www.php.net/min>`_ on an empty array leads to a ``valueError`` `exception <https://www.php.net/exception>`_.

Until PHP 8, `max() <https://www.php.net/max>`_ and `min() <https://www.php.net/min>`_ returned ``null`` in case of empty array. This might be confusing with actual values, as an array can contain ``null``. ``null`` has a specific behavior when comparing with other values, and should be avoided with `max() <https://www.php.net/max>`_ and sorts. 

Until PHP 8.0, a call on an empty array returns `null <https://www.php.net/`null <https://www.php.net/null>`_>`_, and a warning.

.. code-block:: php
   
   <?php
   
   // Throws a value error
   $a = max([]);
   
   $array = [];
   if (empty($array)) {
   	$a = null;
   } else {
   	$a = max($array);
   }
   
   var_dump(min([-1,  null])); // NULL
   var_dump(max([-1,  null])); // -1
   var_dump(max([1,  null]));  // 1
   
   ?>
Related PHP errors 
-------------------

  + `Argument #1 ($value) must contain at least one element <https://php-errors.readthedocs.io/en/latest/messages/must-contain-at-least-one-element.html>`_



Connex PHP features
-------------------

  + `Validation <https://php-dictionary.readthedocs.io/en/latest/dictionary/validation.ini.html>`_


Suggestions
___________

* Check the content of the array before giving it to max() or min()




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/NoMaxOnEmptyArray                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.5.2                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.0 and more recent                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


