.. _structures-assignedinonebranch:


.. _assigned-in-one-branch:

Assigned In One Branch
++++++++++++++++++++++


.. meta::

	:description:

		Assigned In One Branch: This rule reports variables that are assigned in one branch, and not in the other.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Assigned In One Branch

	:twitter:description: Assigned In One Branch: This rule reports variables that are assigned in one branch, and not in the other

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Assigned In One Branch

	:og:type: article

	:og:description: This rule reports variables that are assigned in one branch, and not in the other

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Assigned In One Branch.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AssignedInOneBranch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/AssignedInOneBranch.html","name":"Assigned In One Branch","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This rule reports variables that are assigned in one branch, and not in the other","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Assigned In One Branch.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports variables that are assigned in one branch, and not in the other.

This situation means that, depending on the branch used, some variables may not always be available. Such inbalance may generate warnings. 

This rule looks at if/then structures. 


.. code-block:: php
   
   <?php
   
   if ($condition) {
       // $assigned_in_this_branch is assigned in only one of the branches
       $assigned_in_this_branch = 1;
       $also_assigned = 1;
   } else {
       // $also_assigned is assigned in the two branches
       $also_assigned = 1;
   }
   
   ?>
Connex PHP features
-------------------

  + `assignation <https://php-dictionary.readthedocs.io/en/latest/dictionary/assignation.ini.html>`_


Suggestions
___________

* Assign in the second branch
* Assign outside the condition




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AssignedInOneBranch                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


