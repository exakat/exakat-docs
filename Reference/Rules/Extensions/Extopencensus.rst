.. _extensions-extopencensus:


.. _ext-opencensus:

ext/opencensus
++++++++++++++


.. meta::

	:description:

		ext/opencensus: Extension PHP for OpenCensus.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/opencensus

	:twitter:description: ext/opencensus: Extension PHP for OpenCensus

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/opencensus

	:og:type: article

	:og:description: Extension PHP for OpenCensus

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/opencensus.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extopencensus.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extopencensus.html","name":"ext\/opencensus","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension PHP for OpenCensus","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/opencensus.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension PHP for OpenCensus. 

A stats collection and distributed tracing framework.

.. code-block:: php
   
   <?php
   opencensus_trace_begin('root', ['spanId' => '1234']);
   opencensus_trace_add_annotation('foo');
   opencensus_trace_begin('inner', []);
   opencensus_trace_add_annotation('asdf', ['spanId' => '1234']);
   opencensus_trace_add_annotation('abc');
   opencensus_trace_finish();
   opencensus_trace_finish();
   $traces = opencensus_trace_list();
   echo "Number of traces: " . count($traces) . "\n";
   $span = $traces[0];
   print_r($span->timeEvents());
   $span2 = $traces[1];
   print_r($span2->timeEvents());
   ?>

See also `opencensus <https://github.com/census-instrumentation/opencensus-php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extopencensus                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                                                                                   |
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


