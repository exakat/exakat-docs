.. _php-restrictglobalusage:

.. _restrict-global-usage:

Restrict Global Usage
+++++++++++++++++++++

  $GLOBALS access, as whole, is forbidden. In PHP 8.1, it is not possible to this as a variable, but only access its individual values.

.. code-block:: php
   
   <?php
   // Example extracted from the RFC (see link below)
   // Continues to work:
   foreach ($GLOBALS as $var => $value) {
       echo $var . ' => ' . $value . PHP_EOL;
   }
   
   // Generates compile-time error:
   $GLOBALS = [];
   $GLOBALS += [];
   $GLOBALS =& $x;
   $x =& $GLOBALS;
   unset($GLOBALS);
   
   ?>

See also `Restrict $GLOBALS usage <https://wiki.php.net/rfc/restrict_globals_usage>`_.


Suggestions
___________

* Copy values individually from $GLOBALS




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/RestrictGlobalUsage                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.2                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.1 and more recent                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/GLOBALSAssignement.html>`__                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Features         | global                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


