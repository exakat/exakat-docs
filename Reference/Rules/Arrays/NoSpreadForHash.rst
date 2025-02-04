.. _arrays-nospreadforhash:


.. _no-spread-for-hash:

No Spread For Hash
++++++++++++++++++

.. meta::
	:description:
		No Spread For Hash: The spread operator ``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Spread For Hash
	:twitter:description: No Spread For Hash: The spread operator ``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Spread For Hash
	:og:type: article
	:og:description: The spread operator ``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Spread For Hash.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/NoSpreadForHash.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/NoSpreadForHash.html","name":"No Spread For Hash","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"The spread operator ``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Spread For Hash.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The spread operator ``...`` used to work only on integer-indexed arrays. This limitation was removed in PHP 8.1 and more recent.

.. code-block:: php
   
   <?php
   
   // This is valid, as ``"-33"`` is cast to integer by PHP automagically
   var_dump(...[1,"-33" => 2, 3]);
   
   // This is not valid
   var_dump(...[1,"C" => 2, 3]);
   
   ?>

See also https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list.

Related PHP errors 
-------------------

  + `Cannot unpack array with string keys <https://php-errors.readthedocs.io/en/latest/messages/cannot-unpack-array-with-string-keys.html>`_
  + `array_merge() does not accept unknown named parameters <https://php-errors.readthedocs.io/en/latest/messages/array_merge%28%29-does-not-accept-unknown-named-parameters.html>`_



Connex PHP features
-------------------

  + `Ellipsis <https://php-dictionary.readthedocs.io/en/latest/dictionary/ellipsis.ini.html>`_
  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `Array Spread <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-spread.ini.html>`_


Suggestions
___________

* Add a call to array_values() instead of the hash
* Check the arguments beforehand with array_is_list()
* Upgrade to PHP 8.1




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/NoSpreadForHash                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


