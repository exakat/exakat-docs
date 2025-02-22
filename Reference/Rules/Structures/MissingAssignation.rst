.. _structures-missingassignation:


.. _missing-assignation-in-branches:

Missing Assignation In Branches
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Missing Assignation In Branches: A variable is assigned in one of the branch, but not the other.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Missing Assignation In Branches
	:twitter:description: Missing Assignation In Branches: A variable is assigned in one of the branch, but not the other
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Missing Assignation In Branches
	:og:type: article
	:og:description: A variable is assigned in one of the branch, but not the other
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Missing Assignation In Branches.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MissingAssignation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MissingAssignation.html","name":"Missing Assignation In Branches","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"A variable is assigned in one of the branch, but not the other","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Missing Assignation In Branches.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A variable is assigned in one of the branch, but not the other. Such variable might be needed later, and when going throw this branch, it won't be available. 

In this analysis, elseif() and branches that return or goto somewhere else are omitted. 


.. code-block:: php
   
   <?php
   
   if ($condition) {
     $a = 1;
     $b = 2;
   } else {
     $a = 3;
   }
   
   // $b might be missing
   ?>
Related PHP errors 
-------------------

  + `Undefined variable <https://php-errors.readthedocs.io/en/latest/messages/undefined-variable.html>`_




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MissingAssignation                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
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


