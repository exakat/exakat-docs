.. _performances-avoidarraypush:


.. _avoid-array\_push():

Avoid array_push()
++++++++++++++++++

.. meta::
	:description:
		Avoid array_push(): array_push() is slower than the append ``[]`` operator.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid array_push()
	:twitter:description: Avoid array_push(): array_push() is slower than the append ``[]`` operator
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid array_push()
	:og:type: article
	:og:description: array_push() is slower than the append ``[]`` operator
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid array_push().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/AvoidArrayPush.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/AvoidArrayPush.html","name":"Avoid array_push()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"array_push() is slower than the append ``[]`` operator","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid array_push().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`array_push() <https://www.php.net/array_push>`_ is slower than the append ``[]`` operator.

This is also `true <https://www.php.net/true>`_ when the append operator is called several times, while `array_push() <https://www.php.net/array_push>`_ is be called only once, with an arbitrary number of argument. 

Using count after the push is also faster than collecting `array_push() <https://www.php.net/array_push>`_ return value. 

It is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   $a = [1,2,3];
   // Fast version
   $a[] = 4;
   
   $a[] = 5;
   $a[] = 6;
   $a[] = 7;
   $count = count($a);
   
   // Slow version
   array_push($a, 4);
   $count = array_push($a, 5,6,7);
   
   // Multiple version : 
   $a[] = 1;
   $a[] = 2;
   $a[] = 3;
   array_push($a, 1, 2, 3);
   
   ?>
Connex PHP features
-------------------

  + `Performance <https://php-dictionary.readthedocs.io/en/latest/dictionary/performance.ini.html>`_
  + `Array Append <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-append.ini.html>`_
  + `Array Append <https://php-dictionary.readthedocs.io/en/latest/dictionary/append.ini.html>`_
  + `Array Append <https://php-dictionary.readthedocs.io/en/latest/dictionary/push.ini.html>`_
  + `pop <https://php-dictionary.readthedocs.io/en/latest/dictionary/pop.ini.html>`_


Suggestions
___________

* Use the [] operator




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/AvoidArrayPush                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Performances <ruleset-Performances>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.1                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


