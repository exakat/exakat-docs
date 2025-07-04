.. _performances-doublearrayflip:


.. _double-array\_flip():

Double array_flip()
+++++++++++++++++++

.. meta::
	:description:
		Double array_flip(): Avoid double array_flip() to gain speed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Double array_flip()
	:twitter:description: Double array_flip(): Avoid double array_flip() to gain speed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Double array_flip()
	:og:type: article
	:og:description: Avoid double array_flip() to gain speed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Double array_flip().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/DoubleArrayFlip.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/DoubleArrayFlip.html","name":"Double array_flip()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Avoid double array_flip() to gain speed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Double array_flip().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid double `array_flip() <https://www.php.net/array_flip>`_ to gain speed. While `array_flip() <https://www.php.net/array_flip>`_ alone is usually useful, a double call to `array_flip() <https://www.php.net/array_flip>`_ is made to make values and keys unique.

.. code-block:: php
   
   <?php
   
   // without array_flip
   function foo($array, $value) {
       $key = array_search($array, $value);
       
       if ($key !== false) {
           unset($array[$key]);
       }
       
       return $array;
   }
   
   // double array_flip
   // array_flip() usage means that $array's values are all unique
   function foo($array, $value) {
       $flipped = array_flip($value);
       unset($flipped[$value]);
       return array_flip($flipped);
   }
   
   ?>
Connex PHP features
-------------------

  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `Index For Arrays <https://php-dictionary.readthedocs.io/en/latest/dictionary/index-array.ini.html>`_
  + `array-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-value.ini.html>`_


Suggestions
___________

* Use array_unique() or array_count_values().
* Use array_flip() once, and let PHP garbage collect it later.
* Keep the original values in a separate variable.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/DoubleArrayFlip                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-performances-doublearrayflip`                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


