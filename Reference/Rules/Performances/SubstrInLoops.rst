.. _performances-substrinloops:


.. _substr()-in-loops:

Substr() In Loops
+++++++++++++++++

.. meta::
	:description:
		Substr() In Loops: Successive substr() calls may be replaced by a call to str_split().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Substr() In Loops
	:twitter:description: Substr() In Loops: Successive substr() calls may be replaced by a call to str_split()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Substr() In Loops
	:og:type: article
	:og:description: Successive substr() calls may be replaced by a call to str_split()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Substr() In Loops.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SubstrInLoops.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/SubstrInLoops.html","name":"Substr() In Loops","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"Successive substr() calls may be replaced by a call to str_split()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Substr() In Loops.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Successive `substr() <https://www.php.net/substr>`_ calls may be replaced by a call to `str_split() <https://www.php.net/str_split>`_. 

It speeds up the processing, and allows the replacement of indefinite loops by a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ call. 

This is a micro optimisation. It works better on longer strings.

.. code-block:: php
   
   <?php
   
       $bits = str_split($string, 5);
       foreach($bits as $bit) {
       	foo($bit);
       }
       
       $i = 0;
       $s = strlen($string);
       while($i < $s) {
       	// repeating calls to substr during the loop
       	foo(substr($string, $i * 5, 5));
       	$i += 5;
       }
   
   ?>
Connex PHP features
-------------------

  + `Loops <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Use str_split()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/SubstrInLoops                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


