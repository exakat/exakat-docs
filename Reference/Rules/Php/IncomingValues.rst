.. _php-incomingvalues:

.. _incoming-values:

Incoming Values
+++++++++++++++

.. meta\:\:
	:description:
		Incoming Values: The names of the variables that are passed via the superglobals.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Incoming Values
	:twitter:description: Incoming Values: The names of the variables that are passed via the superglobals
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Incoming Values
	:og:type: article
	:og:description: The names of the variables that are passed via the superglobals
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/IncomingValues.html
	:og:locale: en
  The names of the variables that are passed via the superglobals.

.. code-block:: php
   
   <?php
   
   $x = $_GET['y']; // y is the incoming variable
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/IncomingValues                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.7                                                                                                                   |
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


