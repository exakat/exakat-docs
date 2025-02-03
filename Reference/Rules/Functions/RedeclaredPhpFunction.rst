.. _functions-redeclaredphpfunction:

.. _redeclared-php-functions:

Redeclared PHP Functions
++++++++++++++++++++++++

.. meta::
	:description:
		Redeclared PHP Functions: Function that bear the same name as a PHP function, and that are declared.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Redeclared PHP Functions
	:twitter:description: Redeclared PHP Functions: Function that bear the same name as a PHP function, and that are declared
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Redeclared PHP Functions
	:og:type: article
	:og:description: Function that bear the same name as a PHP function, and that are declared
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Redeclared PHP Functions.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/RedeclaredPhpFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/RedeclaredPhpFunction.html","name":"Redeclared PHP Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Function that bear the same name as a PHP function, and that are declared","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Redeclared PHP Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Function that bear the same name as a PHP function, and that are declared. 

This is useful when managing backward compatibility, like emulating an old function, or preparing for newer PHP versions, like emulating new upcoming function.

.. code-block:: php
   
   <?php
   
   if (version_compare(PHP_VERSION, 7.0) > 0) {
       function split($separator, $string) {
           return explode($separator, $string);
       }
   }
   
   print_r( split(' ', '2 3'));
   
   ?>
Connex PHP features
-------------------

  + `function <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_


Suggestions
___________

* Check if it is still worth emulating that function




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/RedeclaredPhpFunction                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


