.. _extensions-extseaslog:


.. _ext-seaslog:

ext/seaslog
+++++++++++

.. meta::
	:description:
		ext/seaslog: Extension Seaslog.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/seaslog
	:twitter:description: ext/seaslog: Extension Seaslog
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/seaslog
	:og:type: article
	:og:description: Extension Seaslog
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/seaslog.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extseaslog.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extseaslog.html","name":"ext\/seaslog","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension Seaslog","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/seaslog.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension Seaslog.

An effective, fast, stable log extension for PHP.

.. code-block:: php
   
   <?php
   $basePath_1 = SeasLog::getBasePath();
   
   SeasLog::setBasePath('/log/base_test');
   $basePath_2 = SeasLog::getBasePath();
   
   var_dump($basePath_1,$basePath_2);
   
   /*
   string(19) "/log/seaslog-ciogao" 
   string(14) "/log/base_test" 
   */
   
   $lastLogger_1 = SeasLog::getLastLogger();
   
   SeasLog::setLogger('testModule/app1');
   $lastLogger_2 = SeasLog::getLastLogger();
   
   var_dump($lastLogger_1,$lastLogger_2);
   /*
   string(7) "default" 
   string(15) "testModule/app1" 
   */
   ?>

See also `ext/SeasLog on Github <https://github.com/SeasX/SeasLog>`_ and `SeasLog <http://seasx.github.io/SeasLog/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extseaslog                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


