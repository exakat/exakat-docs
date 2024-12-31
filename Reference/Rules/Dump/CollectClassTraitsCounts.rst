.. _dump-collectclasstraitscounts:

.. _collect-class-traits-counts:

Collect Class Traits Counts
+++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Collect Class Traits Counts: This rule counts the number of trait used in a class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Class Traits Counts
	:twitter:description: Collect Class Traits Counts: This rule counts the number of trait used in a class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Class Traits Counts
	:og:type: article
	:og:description: This rule counts the number of trait used in a class
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectClassTraitsCounts.html
	:og:locale: en
  This rule counts the number of trait used in a class. The direct traits are counted, not the traits of the traits.

.. code-block:: php
   
   <?php
   
   // Use no traits
   class x {}
   
   // Use one trait
   class y {
       use TraitT;
   }
   
   ?>
Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectClassTraitsCounts                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


