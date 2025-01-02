.. _structures-vardumpusage:

.. _var\_dump()...-usage:

var_dump()... Usage
+++++++++++++++++++

.. meta::
	:description:
		var_dump()... Usage: var_dump(), print_r() or var_export() should not be left in any production code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: var_dump()... Usage
	:twitter:description: var_dump()... Usage: var_dump(), print_r() or var_export() should not be left in any production code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: var_dump()... Usage
	:og:type: article
	:og:description: var_dump(), print_r() or var_export() should not be left in any production code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/var_dump()... Usage.html
	:og:locale: en
`var_dump() <https://www.php.net/var_dump>`_, `print_r() <https://www.php.net/print_r>`_ or `var_export() <https://www.php.net/var_export>`_ should not be left in any production code. They are debugging functions.
They may be tolerated during development time, but must be removed so as not to have any chance to be run in production.

.. code-block:: php
   
   <?php
   
   if ($error) {
       // Debugging usage of var_dump
       // And major security problem 
       var_dump($query);
       
       // This is OK : the $query is logged, and not displayed
       $this->log(print_r($query, true));
   }
   
   ?>
Connex PHP features
-------------------

  + `debug <https://php-dictionary.readthedocs.io/en/latest/dictionary/debug.ini.html>`_


Suggestions
___________

* Remove usage of var_dump(), print_r(), var_export() without second argument, and other debug functions.
* Push all logging to an external file, instead of the browser.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/VardumpUsage                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-debug-code <https://github.com/dseguy/clearPHP/tree/master/rules/no-debug-code.md>`__                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-structures-vardumpusage`, :ref:`case-piwigo-structures-vardumpusage`                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


