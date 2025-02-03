.. _structures-noarrayunique:

.. _avoid-array\_unique():

Avoid array_unique()
++++++++++++++++++++

.. meta::
	:description:
		Avoid array_unique(): The native function array_unique() is much slower than using other alternatives, such as array_count_values(), array_flip()/array_keys(), or even a foreach() loops.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid array_unique()
	:twitter:description: Avoid array_unique(): The native function array_unique() is much slower than using other alternatives, such as array_count_values(), array_flip()/array_keys(), or even a foreach() loops
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid array_unique()
	:og:type: article
	:og:description: The native function array_unique() is much slower than using other alternatives, such as array_count_values(), array_flip()/array_keys(), or even a foreach() loops
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid array_unique().html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoArrayUnique.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoArrayUnique.html","name":"Avoid array_unique()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The native function array_unique() is much slower than using other alternatives, such as array_count_values(), array_flip()\/array_keys(), or even a foreach() loops","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid array_unique().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The native function `array_unique() <https://www.php.net/array_unique>`_ is much slower than using other alternatives, such as `array_count_values() <https://www.php.net/array_count_values>`_, `array_flip() <https://www.php.net/array_flip>`_/`array_keys() <https://www.php.net/array_keys>`_, or even a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops.

.. code-block:: php
   
   <?php
   
   // using array_unique()
   $uniques = array_unique($someValues);
   
   // When values are strings or integers
   $uniques = array_keys(array_count_values($someValues));
   $uniques = array_flip(array_flip($someValues))
   
   //even some loops are faster.
   $uniques = [];
   foreach($someValues as $s) {
       if (!in_array($uniques, $s)) {
           $uniques[] $s;
       }
   }
   
   ?>

See also `array_unique <https://www.php.net/array_unique>`_..

Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Upgrade to PHP 7.2
* Use an alternative way to make values unique in an array, using array_count_values(), for example.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoArrayUnique                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.2 and older                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


