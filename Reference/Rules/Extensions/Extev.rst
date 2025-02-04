.. _extensions-extev:


.. _ext-ev:

ext/ev
++++++

.. meta::
	:description:
		ext/ev: Extension ev.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ev
	:twitter:description: ext/ev: Extension ev
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ev
	:og:type: article
	:og:description: Extension ev
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/ev.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extev.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extev.html","name":"ext\/ev","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ev","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/ev.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ev.

ext/ev is a high performance full-featured event loop written in C.

.. code-block:: php
   
   <?php
   // Create and start timer firing after 2 seconds
   $w1 = new EvTimer(2, 0, function () {
       echo '2 seconds elapsed'.PHP_EOL;
   });
   
   // Create and launch timer firing after 2 seconds repeating each second
   // until we manually stop it
   $w2 = new EvTimer(2, 1, function ($w) {
       echo 'is called every second, is launched after 2 seconds'.PHP_EOL;
       echo 'iteration = ', Ev::iteration(), PHP_EOL;
   
       // Stop the watcher after 5 iterations
       Ev::iteration() == 5 and $w->stop();
       // Stop the watcher if further calls cause more than 10 iterations
       Ev::iteration() >= 10 and $w->stop();
   });
   
   // Create stopped timer. It will be inactive until we start it ourselves
   $w_stopped = EvTimer::createStopped(10, 5, function($w) {
       echo 'Callback of a timer created as stopped'.PHP_EOL;
   
       // Stop the watcher after 2 iterations
       Ev::iteration() >= 2 and $w->stop();
   });
   
   // Loop until Ev::stop() is called or all of watchers stop
   Ev::run();
   
   // Start and look if it works
   $w_stopped->start();
   echo 'Run single iteration'.PHP_EOL;
   Ev::run(Ev::RUN_ONCE);
   
   echo 'Restart the second watcher and try to handle the same events, but don\'t block'.PHP_EOL;
   $w2->again();
   Ev::run(Ev::RUN_NOWAIT);
   
   $w = new EvTimer(10, 0, function() {});
   echo 'Running a blocking loop'.PHP_EOL;
   Ev::run();
   echo 'END'.PHP_EOL;
   ?>

See also `Ev <https://www.php.net/manual/en/book.ev.php>`_ and `libev <http://software.schmorp.de/pkg/libev.html>`_.

Connex PHP features
-------------------

  + `Event Loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/event-loop.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extev                                                                                                                                                                        |
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


