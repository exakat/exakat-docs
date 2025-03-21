.. _structures-toomanyelseif:


.. _too-many-stringed-elseif:

Too Many Stringed Elseif
++++++++++++++++++++++++

.. meta::
	:description:
		Too Many Stringed Elseif: Too many if/then structures are linked.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Many Stringed Elseif
	:twitter:description: Too Many Stringed Elseif: Too many if/then structures are linked
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Many Stringed Elseif
	:og:type: article
	:og:description: Too many if/then structures are linked
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Too Many Stringed Elseif.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/TooManyElseif.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/TooManyElseif.html","name":"Too Many Stringed Elseif","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Too many if\/then structures are linked","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Too Many Stringed Elseif.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Too many if/then structures are linked. If a pattern emerges, such as with the illustration below, they might be replaced with a loop, a `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ or a `match() <https://www.php.net/manual/en/control-structures.match.php>`_ statement. 

This rule also takes into account ``else if`` structures.

.. code-block:: php
   
   <?php
   
   if      ($a === 1) {   }
   elseif  ($a === 2) {   }
   elseif  ($a === 3) {   }
   else if ($a === 4) {   } // else if
   elseif  ($a === 5) {   }
   
   ?>

+-------+---------+---------+--------------------------------------------------------------+
| Name  | Default | Type    | Description                                                  |
+-------+---------+---------+--------------------------------------------------------------+
| maxIf | 5       | integer | Maximum number of allowed stringed if-then-elseif structure. |
+-------+---------+---------+--------------------------------------------------------------+



See also :ref:`Bail Out Early <bail-out-early>`.


Suggestions
___________

* Replace the if-then with a loop
* Use the bail early strategy to isolate the if-then




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/TooManyElseif                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


