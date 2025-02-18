.. _performances-autoappend:


.. _autoappend:

Autoappend
++++++++++

.. meta::
	:description:
		Autoappend: Appending a variable to itself leads to exponential usage of memory.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Autoappend
	:twitter:description: Autoappend: Appending a variable to itself leads to exponential usage of memory
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Autoappend
	:og:type: article
	:og:description: Appending a variable to itself leads to exponential usage of memory
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Autoappend.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/Autoappend.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/Autoappend.html","name":"Autoappend","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 11 Feb 2025 09:13:38 +0000","dateModified":"Tue, 11 Feb 2025 09:13:38 +0000","description":"Appending a variable to itself leads to exponential usage of memory","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Autoappend.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Appending a variable to itself leads to exponential usage of memory. Each time, the size of the variable is doubled. It is recommended to avoid using so much memory.

.. code-block:: php
   
   <?php
   
   // Always append a value to a distinct variable
   foreach($a as $b) {
       $c[] = $b;
   }
   
   // This copies the array to itself, and double the size each loop
   foreach($a as $b) {
       $c[] = $c;
   }
   
   ?>
Connex PHP features
-------------------

  + `Performance <https://php-dictionary.readthedocs.io/en/latest/dictionary/performance.ini.html>`_
  + `Array Append <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-append.ini.html>`_


Suggestions
___________

* Change the variable on the left of the append
* Change the variable on the right of the append




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/Autoappend                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


