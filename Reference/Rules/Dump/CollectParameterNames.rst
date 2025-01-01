.. _dump-collectparameternames:

.. _collect-parameter-names:

Collect Parameter Names
+++++++++++++++++++++++

.. meta::
	:description:
		Collect Parameter Names: This analysis collects the names of all parameters.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Parameter Names
	:twitter:description: Collect Parameter Names: This analysis collects the names of all parameters
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Parameter Names
	:og:type: article
	:og:description: This analysis collects the names of all parameters
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectParameterNames.html
	:og:locale: en
This analysis collects the names of all parameters. It also counts the number of occurrences of each name.

The names are collected from functions, methods, closures and arrow functions. Compulsory and optional parameters are all processed.

.. code-block:: php
   
   <?php
   
   // parameter $a
   function foo($a) { }
   
   // parameter $b, $c
   function ($b, $c = 2) {}
   
   // parameters in interfaces are counted too.
   // Here, $a will be counted with the one above.
   interfaces x {
       function moo($a);
   }
   ?>
Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectParameterNames                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


