.. _structures-repeatedprint:

.. _repeated-print():

Repeated print()
++++++++++++++++

.. meta::
	:description:
		Repeated print(): Merge several print or echo in one call, to speed up the processing.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Repeated print()
	:twitter:description: Repeated print(): Merge several print or echo in one call, to speed up the processing
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Repeated print()
	:og:type: article
	:og:description: Merge several print or echo in one call, to speed up the processing
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Repeated print().html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RepeatedPrint.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/RepeatedPrint.html","name":"Repeated print()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Merge several print or echo in one call, to speed up the processing","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Repeated print().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Merge several print or echo in one call, to speed up the processing.

It is recommended to use echo with multiple arguments, or a concatenation with print, instead of multiple calls to print echo, when outputting several blob of text.

.. code-block:: php
   
   <?php
   
   //Write : 
     echo 'a', $b, 'c';
     print 'a' . $b . 'c';
   
   //Don't write :  
     print 'a';
     print $b;
     print 'c';
   ?>
Connex PHP features
-------------------

  + `print <https://php-dictionary.readthedocs.io/en/latest/dictionary/print.ini.html>`_


Suggestions
___________

* Merge all prints into one echo call, separating arguments by commas.
* Collect all values in one variable, and do only one call to print or echo.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RepeatedPrint                                                                                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-repeated-print <https://github.com/dseguy/clearPHP/tree/master/rules/no-repeated-print.md>`__                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-edusoho-structures-repeatedprint`, :ref:`case-humo-gen-structures-repeatedprint`                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


