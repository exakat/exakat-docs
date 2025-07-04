.. _structures-gotokeydirectly:


.. _find-key-directly:

Find Key Directly
+++++++++++++++++

.. meta::
	:description:
		Find Key Directly: There is no need to use foreach() to search for a key.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Find Key Directly
	:twitter:description: Find Key Directly: There is no need to use foreach() to search for a key
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Find Key Directly
	:og:type: article
	:og:description: There is no need to use foreach() to search for a key
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Find Key Directly.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/GoToKeyDirectly.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/GoToKeyDirectly.html","name":"Find Key Directly","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"There is no need to use foreach() to search for a key","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Find Key Directly.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There is no need to use `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ to search for a key. 

PHP offers two solutions : `array_search() <https://www.php.net/array_search>`_ and `array_keys() <https://www.php.net/array_keys>`_. `Array_search() <https://www.php.net/array_search>`_ finds the first key that fits a value, and `array_keys() <https://www.php.net/array_keys>`_ returns all the keys.

.. code-block:: php
   
   <?php
   
   $array = ['a', 'b', 'c', 'd', 'e'];
   
   print array_search($array, 'c'); 
   // print 2 => 'c';
   
   print_r(array_keys($array, 'c')); 
   // print 2 => 'c';
   
   ?>

See also `array_search <https://www.php.net/array_search>`_ and `array_keys <https://www.php.net/array_keys>`_.

Connex PHP features
-------------------

  + `Properties <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Use array_search()
* Use array_keys()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/GoToKeyDirectly                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


