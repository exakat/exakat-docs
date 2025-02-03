.. _php-restrictglobalusage:


.. _restrict-global-usage:

Restrict Global Usage
+++++++++++++++++++++

.. meta::
	:description:
		Restrict Global Usage: $GLOBALS access, as whole, is forbidden.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Restrict Global Usage
	:twitter:description: Restrict Global Usage: $GLOBALS access, as whole, is forbidden
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Restrict Global Usage
	:og:type: article
	:og:description: $GLOBALS access, as whole, is forbidden
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Restrict Global Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/RestrictGlobalUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/RestrictGlobalUsage.html","name":"Restrict Global Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"$GLOBALS access, as whole, is forbidden","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Restrict Global Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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

Related PHP errors 
-------------------

  + `$GLOBALS can only be modified using the $GLOBALS[$name] = $value syntax <https://php-errors.readthedocs.io/en/latest/messages/%24globals-can-only-be-modified-using-the-%24globals%5B%24name%5D-%3D-%24value-syntax.html>`_



Connex PHP features
-------------------

  + `global <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_


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
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


