.. _structures-doubleassignation:

.. _double-assignation:

Double Assignation
++++++++++++++++++

.. meta::
	:description:
		Double Assignation: This happens when a container (variable, property, array index) is assigned with values twice in a row.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Double Assignation
	:twitter:description: Double Assignation: This happens when a container (variable, property, array index) is assigned with values twice in a row
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Double Assignation
	:og:type: article
	:og:description: This happens when a container (variable, property, array index) is assigned with values twice in a row
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Double Assignation.html
	:og:locale: en
This happens when a container (variable, property, array index) is assigned with values twice in a row. One of them is probably a debug instruction, that was forgotten.

.. code-block:: php
   
   <?php
   
   // Normal assignation
   $a = 1;
   
   // Double assignation
   $b = 2;
   $b = 3;
   
   ?>
Connex PHP features
-------------------

  + `assignation <https://php-dictionary.readthedocs.io/en/latest/dictionary/assignation.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DoubleAssignation                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


