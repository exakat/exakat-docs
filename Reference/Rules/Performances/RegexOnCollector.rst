.. _performances-regexoncollector:


.. _processing-collector:

Processing Collector
++++++++++++++++++++

.. meta::
	:description:
		Processing Collector: When accumulating data in a variable, within a loop, it is slow to apply repeatedly a function to the variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Processing Collector
	:twitter:description: Processing Collector: When accumulating data in a variable, within a loop, it is slow to apply repeatedly a function to the variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Processing Collector
	:og:type: article
	:og:description: When accumulating data in a variable, within a loop, it is slow to apply repeatedly a function to the variable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Processing Collector.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/RegexOnCollector.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/RegexOnCollector.html","name":"Processing Collector","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 11 Feb 2025 09:13:38 +0000","dateModified":"Tue, 11 Feb 2025 09:13:38 +0000","description":"When accumulating data in a variable, within a loop, it is slow to apply repeatedly a function to the variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Processing Collector.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When accumulating data in a variable, within a loop, it is slow to apply repeatedly a function to the variable.

The example below illustrate the problem : ``$collector`` is build with element from ``$array``. ``$collector`` actually gets larger and larger, slowing the `in_array() <https://www.php.net/in_array>`_ call each time. 

It is better to apply the `preg_replace() <https://www.php.net/preg_replace>`_ to ``$a``, a short variable, and then, add ``$a`` to the collector.

.. code-block:: php
   
   <?php
   
   // Fast way
   $collector = '';
   foreach($array as $a){
       $a = preg_replace('/__(.*?)__/', '<b>$1</b>', $a);
       $collector .= $a;
   }
   
   // Slow way
   $collector = '';
   foreach($array as $a){
       $collector .= $a;
       $collector = preg_replace('/__(.*?)__/', '<b>$1</b>', $collector);
   }
   
   ?>
Connex PHP features
-------------------

  + `Regular Expressions <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_
  + `collector <https://php-dictionary.readthedocs.io/en/latest/dictionary/collector.ini.html>`_


Suggestions
___________

* Avoid applying the checks on the whole data, rather on the diff only.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/RegexOnCollector                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


