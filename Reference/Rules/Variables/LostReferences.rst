.. _variables-lostreferences:


.. _lost-references:

Lost References
+++++++++++++++

.. meta::
	:description:
		Lost References: Either avoid references, or propagate them correctly.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Lost References
	:twitter:description: Lost References: Either avoid references, or propagate them correctly
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Lost References
	:og:type: article
	:og:description: Either avoid references, or propagate them correctly
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Lost References.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/LostReferences.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/LostReferences.html","name":"Lost References","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Either avoid references, or propagate them correctly","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Lost References.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Either avoid references, or propagate them correctly.

When assigning a referenced variable with another reference, the initial reference is lost, while the intend was to transfer the content. 
Do not reassign a reference with another reference. Assign new content to the reference to change its value.

.. code-block:: php
   
   <?php
   
   function foo(&$lostReference, &$keptReference)
   {
       $c = 'c';
   
       // $lostReference was a reference to $bar, but now, it is a reference to $c
       $lostReference =& $c;
       // $keptReference was a reference to $bar : it is still now, though it contains the actual value of $c now
       $keptReference = $c;
   }
   
   $bar = 'bar';
   $bar2 = 'bar';
   foo($bar, $bar2); 
   
   //displays bar c, instead of bar bar
   print $bar. ' '.$bar2;
   
   ?>
Connex PHP features
-------------------

  + `References <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Suggestions
___________

* Always assign new value to an referenced argument, and don't reassign a new reference




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/LostReferences                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-variables-lostreferences`                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


