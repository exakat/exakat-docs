.. _performances-issetwholearray:


.. _isset()-on-the-whole-array:

Isset() On The Whole Array
++++++++++++++++++++++++++


.. meta::

	:description:

		Isset() On The Whole Array: Isset() works quietly on a whole array.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Isset() On The Whole Array

	:twitter:description: Isset() On The Whole Array: Isset() works quietly on a whole array

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Isset() On The Whole Array

	:og:type: article

	:og:description: Isset() works quietly on a whole array

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Isset() On The Whole Array.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/IssetWholeArray.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/IssetWholeArray.html","name":"Isset() On The Whole Array","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Isset() works quietly on a whole array","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Isset() On The Whole Array.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Isset() <https://www.www.php.net/isset>`_ works quietly on a whole array. There is no need to test all previous index before testing for the target index.

It also works on chained properties. 
There is a gain in readability, by avoiding long and hard to read logical expression, and reducing them in one simple `isset() <https://www.www.php.net/isset>`_ call.

There is a gain in performances by using one call to `isset() <https://www.www.php.net/isset>`_, instead of several. It is a micro-optimization.

.. code-block:: php
   
   <?php
   
   // Straight to the point
   if (isset($a[1]['source'])) {
       // Do something with $a[1]['source']
   }
   
   // Doing too much work
   if (isset($a) && isset($a[1]) && isset($a[1]['source'])) {
       // Do something with $a[1]['source']
   }
   
   // Doing too much work
   if (isset($object) && isset($object->p1) && isset($object->p1->property)) {
       // Do something with $object->p1->property
   }
   
   ?>

See also `Isset <http://www.php.net/isset>`_.

Connex PHP features
-------------------

  + `coalesce <https://php-dictionary.readthedocs.io/en/latest/dictionary/coalesce.ini.html>`_
  + `isset <https://php-dictionary.readthedocs.io/en/latest/dictionary/isset.ini.html>`_


Suggestions
___________

* Merge all calls in one, and remove all unnecessary calls to isset()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/IssetWholeArray                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.6                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-performances-issetwholearray`, :ref:`case-expressionengine-performances-issetwholearray`                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


