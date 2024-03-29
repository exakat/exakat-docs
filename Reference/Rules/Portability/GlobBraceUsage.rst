.. _portability-globbraceusage:

.. _glob\_brace-usage:

GLOB_BRACE Usage
++++++++++++++++

  `GLOB_BRACE <https://www.php.net/GLOB_BRACE>`_ is not always available on every underlying operating system. This is the case on Solaris OS, and on Alpine OS, used for Docker.
It is possible to check the support for `GLOB_BRACE <https://www.php.net/GLOB_BRACE>`_ by checking the presence of the constant.

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
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
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
| Features     | glob                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


