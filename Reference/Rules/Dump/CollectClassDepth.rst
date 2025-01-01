.. _dump-collectclassdepth:

.. _collect-class-depth:

Collect Class Depth
+++++++++++++++++++

.. meta::
	:description:
		Collect Class Depth: This rule count the number of level of extends in classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Class Depth
	:twitter:description: Collect Class Depth: This rule count the number of level of extends in classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Class Depth
	:og:type: article
	:og:description: This rule count the number of level of extends in classes
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectClassDepth.html
	:og:locale: en
This rule count the number of level of extends in classes. Each level is a depth level: the last child has that number of direct `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, which are dependencies.

.. code-block:: php
   
   <?php
   
   class a {}
   
   class b extends a {}
   
   class c extends b {}
   
   class d extends a {}
   ?>
Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectClassDepth                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.3                                                                                                                                                                                   |
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


