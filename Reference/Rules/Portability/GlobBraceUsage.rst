.. _portability-globbraceusage:


.. _glob\_brace-usage:

GLOB_BRACE Usage
++++++++++++++++

.. meta::
	:description:
		GLOB_BRACE Usage: GLOB_BRACE is not always available on every underlying operating system.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: GLOB_BRACE Usage
	:twitter:description: GLOB_BRACE Usage: GLOB_BRACE is not always available on every underlying operating system
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: GLOB_BRACE Usage
	:og:type: article
	:og:description: GLOB_BRACE is not always available on every underlying operating system
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/GLOB_BRACE Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Portability\/GlobBraceUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Portability\/GlobBraceUsage.html","name":"GLOB_BRACE Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"GLOB_BRACE is not always available on every underlying operating system","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/GLOB_BRACE Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`GLOB_BRACE <https://www.php.net/glob_brace>`_ is not always available on every underlying operating system. This is the case on Solaris OS, and on Alpine OS, used for Docker.
It is possible to check the support for `GLOB_BRACE <https://www.php.net/glob_brace>`_ by checking the presence of the constant.

.. code-block:: php
   
   <?php
   
   // glob uses GLOB_BRACE
   $abcFiles = glob($path.'/{a,b,c}*', GLOB_BRACE); 
   
   // avoiding usage of GLOB_BRACE
   $abcFiles = array_merge(glob($path.'/a*'), 
                           glob($path.'/b*'), 
                           glob($path.'/c*'), 
                          ); 
   
   ?>

See also `Alpine Linux <https://alpinelinux.org/>`_, `GLOB_BRACE breaks Sulu on Alpine Linux <https://github.com/sulu/sulu/issues/4513>`_ and `[performance] Symfony Kernel::boot() in dev mode on Alpine #35009 <https://github.com/symfony/symfony/issues/35009>`_.

Connex PHP features
-------------------

  + `glob() <https://php-dictionary.readthedocs.io/en/latest/dictionary/glob.ini.html>`_


Suggestions
___________

* Create as many glob() calls at there are alternative in the braces
* Use another tool to search the system on names
* Do not use glob brace




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Portability/GlobBraceUsage                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


