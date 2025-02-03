.. _structures-unsetinforeach:


.. _unset-in-foreach:

Unset In Foreach
++++++++++++++++

.. meta::
	:description:
		Unset In Foreach: Unset applied to the variables of a ``foreach`` loop are useless.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unset In Foreach
	:twitter:description: Unset In Foreach: Unset applied to the variables of a ``foreach`` loop are useless
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unset In Foreach
	:og:type: article
	:og:description: Unset applied to the variables of a ``foreach`` loop are useless
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unset In Foreach.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnsetInForeach.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnsetInForeach.html","name":"Unset In Foreach","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Unset applied to the variables of a ``foreach`` loop are useless","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unset In Foreach.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Unset applied to the variables of a ``foreach`` loop are useless. Those variables are copies and not the actual value. Even if the value is a reference, unsetting it has no effect on the original array : the only effect may be indirect, on elements inside an array, or on properties inside an object.

.. code-block:: php
   
   <?php
   
   // When unset is useless
   $array = [1, 2, 3];
   foreach($array as $a) {
       unset($a);
   }
   
   print_r($array); // still [1, 2, 3]
   
   foreach($array as $b => &$a) {
       unset($a);
   }
   
   print_r($array); // still [1, 2, 3]
   
   // When unset is useful
   $array = [ [ 'c' => 1] ]; // Array in array
   foreach($array as &$a) {
       unset(&$a['c']);
   }
   
   print_r($array); // now [ ['c' => null] ]
   
   ?>
Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Suggestions
___________

* Drop the unset




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnsetInForeach                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


