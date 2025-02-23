.. _extensions-extxhprof:


.. _ext-xhprof:

ext/xhprof
++++++++++

.. meta::
	:description:
		ext/xhprof: Extension xhprof.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xhprof
	:twitter:description: ext/xhprof: Extension xhprof
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xhprof
	:og:type: article
	:og:description: Extension xhprof
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/xhprof.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extxhprof.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extxhprof.html","name":"ext\/xhprof","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension xhprof","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/xhprof.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension xhprof.

XHProf is a light-weight hierarchical and instrumentation based profiler.

.. code-block:: php
   
   <?php
   xhprof_enable(XHPROF_FLAGS_CPU + XHPROF_FLAGS_MEMORY);
   
   for ($i = 0; $i <= 1000; $i++) {
       $a = $i * $i;
   }
   
   $xhprof_data = xhprof_disable();
   
   $XHPROF_ROOT = '/tools/xhprof/';
   include_once $XHPROF_ROOT . '/xhprof_lib/utils/xhprof_lib.php';
   include_once $XHPROF_ROOT . '/xhprof_lib/utils/xhprof_runs.php';
   
   $xhprof_runs = new XHProfRuns_Default();
   $run_id = $xhprof_runs->save_run($xhprof_data, 'xhprof_testing');
   
   echo 'http://localhost/xhprof/xhprof_html/index.php?run={$run_id}&source=xhprof_testing'.PHP_EOL;
   
   ?>

See also `XHprof Documentation <http://web.archive.org/web/20110514095512/http://mirror.facebook.net/facebook/xhprof/doc.html>`_ and `ext/apcu <https://pecl.php.net/package/xhprof>`_.

Connex PHP features
-------------------

  + `PHP Profiler <https://php-dictionary.readthedocs.io/en/latest/dictionary/profiler.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxhprof                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


