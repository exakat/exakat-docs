.. _dump-collectclasschanges:

.. _collect-static-class-changes:

Collect Static Class Changes
++++++++++++++++++++++++++++

.. meta::
	:description:
		Collect Static Class Changes: Collects changes to constants, methods and properties, within a class hierarchy.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Static Class Changes
	:twitter:description: Collect Static Class Changes: Collects changes to constants, methods and properties, within a class hierarchy
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Static Class Changes
	:og:type: article
	:og:description: Collects changes to constants, methods and properties, within a class hierarchy
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Static Class Changes.html
	:og:locale: en
Collects changes to constants, methods and properties, within a class hierarchy. It reports changes in visibility, type and values for constants; visibility, type and values for properties.

.. code-block:: php
   
   <?php
   
   class x {
       protected $property = 1;
       
       protected function method() {}
   }
   
   class y extends x {
       // $property is changed
       protected $property = 2;
       
       // method is not changed
       protected function method() {}
   }
   
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectClassChanges                                                                                                                                                                |
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


