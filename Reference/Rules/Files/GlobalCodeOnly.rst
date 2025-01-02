.. _files-globalcodeonly:

.. _global-code-only:

Global Code Only
++++++++++++++++

.. meta::
	:description:
		Global Code Only: This rule reports files that only contain global code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Global Code Only
	:twitter:description: Global Code Only: This rule reports files that only contain global code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Global Code Only
	:og:type: article
	:og:description: This rule reports files that only contain global code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Global Code Only.html
	:og:locale: en
This rule reports files that only contain global code.

.. code-block:: php
   
   <?php
   
   include 'another_file.pnp';
   
   // This sets an options, but does not execute anything
   set_memory_limit(-1);
   
   // Some definitions, no code 
   const A = 1;
   
   function foo() {}
   
   class x {}
   
   ?>
Connex PHP features
-------------------

  + `global-code <https://php-dictionary.readthedocs.io/en/latest/dictionary/global-code.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Files/GlobalCodeOnly                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


