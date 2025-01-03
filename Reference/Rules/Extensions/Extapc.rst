.. _extensions-extapc:

.. _ext-apc:

ext/apc
+++++++

.. meta::
	:description:
		ext/apc: Extension Alternative PHP Cache.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/apc
	:twitter:description: ext/apc: Extension Alternative PHP Cache
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/apc
	:og:type: article
	:og:description: Extension Alternative PHP Cache
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/apc.html
	:og:locale: en
Extension Alternative PHP Cache.

The Alternative PHP Cache (APC) is a free and open opcode cache for PHP. Its goal is to provide a free, open, and robust framework for caching and optimizing PHP intermediate code.

This extension is considered unmaintained and dead.

.. code-block:: php
   
   <?php
      $bar = 'BAR';
      apc_add('foo', $bar);
      var_dump(apc_fetch('foo'));
      echo PHP_EOL;
   
      $bar = 'NEVER GETS SET';
      apc_add('foo', $bar);
      var_dump(apc_fetch('foo'));
      echo PHP_EOL;
   ?>

See also `Alternative PHP Cache <https://www.php.net/apc>`_.


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extapc                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


