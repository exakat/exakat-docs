.. _dump-collectsnames:

.. _collects-names:

Collects Names
++++++++++++++

.. meta\:\:
	:description:
		Collects Names: Collects the names used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collects Names
	:twitter:description: Collects Names: Collects the names used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collects Names
	:og:type: article
	:og:description: Collects the names used in the code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectsNames.html
	:og:locale: en
  Collects the names used in the code. Names are extracted from namespaces, classes, interfaces, traits, enumerations, variables (parameter and local variable), properties, constants, methods, functions, use expression (with as). 

Variables names are trimmed of their ``$`` sign. Namespaces are kept as a whole. Each name has the type from the code.

The following code provides 3 values ; ``parameter``, ``foo`` and ``local``.

.. code-block:: php
   
   <?php
   
   function foo($parameter) {
   	$local = $parameter;
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectsNames                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


