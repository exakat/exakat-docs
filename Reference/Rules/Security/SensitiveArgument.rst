.. _security-sensitiveargument:

.. _sensitive-argument:

Sensitive Argument
++++++++++++++++++

.. meta::
	:description:
		Sensitive Argument: Spot the argument that are sensitive for security.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Sensitive Argument
	:twitter:description: Sensitive Argument: Spot the argument that are sensitive for security
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Sensitive Argument
	:og:type: article
	:og:description: Spot the argument that are sensitive for security
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Sensitive Argument.html
	:og:locale: en
Spot the argument that are sensitive for security. The functioncalls that are hosting a sensitive argument are called a sink.

.. code-block:: php
   
   <?php
   
   // first argument $query is a sensitive argument 
   mysqli_query($query);
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/SensitiveArgument                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


