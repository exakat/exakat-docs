.. _structures-arrayfillwithobjects:


.. _array\_fill()-with-objects:

Array_Fill() With Objects
+++++++++++++++++++++++++

.. meta::
	:description:
		Array_Fill() With Objects: array_fill() fills an array with identical objects, not copies nor clones.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Array_Fill() With Objects
	:twitter:description: Array_Fill() With Objects: array_fill() fills an array with identical objects, not copies nor clones
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Array_Fill() With Objects
	:og:type: article
	:og:description: array_fill() fills an array with identical objects, not copies nor clones
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Array_Fill() With Objects.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayFillWithObjects.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ArrayFillWithObjects.html","name":"Array_Fill() With Objects","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"array_fill() fills an array with identical objects, not copies nor clones","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Array_Fill() With Objects.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`array_fill() <https://www.php.net/array_fill>`_ fills an array with identical objects, not copies nor clones. This means that all the filled objects are a reference to the same object. Changing one of them will change any of them.

Make sure this is the intended effect in the code. 

This applies to `array_pad() <https://www.php.net/array_pad>`_ too. It doesn't apply to `array_fill_keys() <https://www.php.net/array_fill_keys>`_, as objects will be cast to a string before usage in this case. 



.. code-block:: php
   
   <?php
   
   $x = new StdClass();
   $array = array_fill(0, 10, $x);
   
   $array[3]->y = "Set in object #3";
   
   // displays "Set in object #3" 
   echo $array[5]->y;
   
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `object <https://php-dictionary.readthedocs.io/en/latest/dictionary/object.ini.html>`_


Suggestions
___________

* Use a loop to fill in the array with cloned() objects.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayFillWithObjects                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


