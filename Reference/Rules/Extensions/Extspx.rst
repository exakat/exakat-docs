.. _extensions-extspx:

.. _ext-spx:

ext/spx
+++++++

.. meta::
	:description:
		ext/spx: SPX, which stands for Simple Profiling eXtension, is just another profiling extension for PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/spx
	:twitter:description: ext/spx: SPX, which stands for Simple Profiling eXtension, is just another profiling extension for PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/spx
	:og:type: article
	:og:description: SPX, which stands for Simple Profiling eXtension, is just another profiling extension for PHP
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extspx.html
	:og:locale: en
SPX, which stands for Simple Profiling eXtension, is just another profiling extension for PHP.

.. code-block:: php
   
   <?php
   
   while ($task = get_next_ready_task()) {
     spx_profiler_start();
     try {
       $task->process();
     } finally {
       spx_profiler_stop();
     }
   }
   ?>

See also `<https://github.com/NoiseByNorthwest/php-spx>`_.

Connex PHP features
-------------------

  + `profiler <https://php-dictionary.readthedocs.io/en/latest/dictionary/profiler.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extspx                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


