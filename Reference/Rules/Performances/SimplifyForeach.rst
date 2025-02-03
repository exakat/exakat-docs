.. _performances-simplifyforeach:


.. _simplify-foreach:

Simplify Foreach
++++++++++++++++


.. meta::

	:description:

		Simplify Foreach: Remove all unused keys or values from a foreach() call.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Simplify Foreach

	:twitter:description: Simplify Foreach: Remove all unused keys or values from a foreach() call

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Simplify Foreach

	:og:type: article

	:og:description: Remove all unused keys or values from a foreach() call

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Simplify Foreach.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SimplifyForeach.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SimplifyForeach.html","name":"Simplify Foreach","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Remove all unused keys or values from a foreach() call","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Simplify Foreach.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Remove all unused keys or values from a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ call. This prevents PHP from assigning them for nothing, and save some processing time. 
This is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   // No key usage
   foreach($array as $key => $value) {
       echo $value;
   }
   
   // No value usage
   foreach($array as $key => $value) {
       echo $key;
   }
   
   ?>
Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Suggestions
___________

* Use array_keys() or array_values() to simplify the source array
* Remove the call to $key => when the key is not used in the loop




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SimplifyForeach                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.7                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


