.. _extensions-exthrtime:


.. _ext-hrtime:

ext/hrtime
++++++++++


.. meta::

	:description:

		ext/hrtime: High resolution timing Extension.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/hrtime

	:twitter:description: ext/hrtime: High resolution timing Extension

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/hrtime

	:og:type: article

	:og:description: High resolution timing Extension

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/hrtime.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Exthrtime.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Exthrtime.html","name":"ext\/hrtime","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"High resolution timing Extension","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/hrtime.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

High resolution timing Extension.

The HRTime extension implements a high resolution `StopWatch` class. It uses the best possible API on different platforms which brings resolution up to nanoseconds. It also makes possible to implement a custom stopwatch using low level ticks delivered by the underlaying system.

.. code-block:: php
   
   <?php
   
   $c = new HRTime\StopWatch;
   
   $c->start();
   /* measure this code block execution */
   for ($i = 0; $i < 1024*1024; $i++);
   $c->stop();
   $elapsed0 = $c->getLastElapsedTime(HRTime\Unit::NANOSECOND);
   
   /* measurement is not running here*/
   for ($i = 0; $i < 1024*1024; $i++);
   
   $c->start();
   /* measure this code block execution */
   for ($i = 0; $i < 1024*1024; $i++);
   $c->stop();
   $elapsed1 = $c->getLastElapsedTime(HRTime\Unit::NANOSECOND);
   
   $elapsed_total = $c->getElapsedTime(HRTime\Unit::NANOSECOND);
   
   ?>

See also `ext/hrtime manual <https://www.php.net/manual/en/intro.hrtime.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exthrtime                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.5                                                                                                                                                                                   |
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


