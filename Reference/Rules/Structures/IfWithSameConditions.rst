.. _structures-ifwithsameconditions:

.. _if-with-same-conditions:

If With Same Conditions
+++++++++++++++++++++++

.. meta::
	:description:
		If With Same Conditions: Successive If / then structures that have the same condition may be either merged or have one of the condition changed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: If With Same Conditions
	:twitter:description: If With Same Conditions: Successive If / then structures that have the same condition may be either merged or have one of the condition changed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: If With Same Conditions
	:og:type: article
	:og:description: Successive If / then structures that have the same condition may be either merged or have one of the condition changed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/If With Same Conditions.html
	:og:locale: en
Successive If / then structures that have the same condition may be either merged or have one of the condition changed. 
Note that if the values used in the condition have been modified in the first if/then structure, the two distinct conditions may be needed.

.. code-block:: php
   
   <?php
   
   if ($a == 1) {
       doSomething();
   }
   
   if ($a == 1) {
       doSomethingElse();
   }
   
   // May be replaced by 
   if ($a == 1) {
       doSomething();
       doSomethingElse();
   }
   
   ?>

Suggestions
___________

* Merge the two conditions so the condition is used once.
* Change one of the condition, so they are different
* Make it obvious that the first condition is a try, preparing the normal conditions.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IfWithSameConditions                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpmyadmin-structures-ifwithsameconditions`, :ref:`case-phpdocumentor-structures-ifwithsameconditions`                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


