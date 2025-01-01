.. _structures-mergeifthen:

.. _merge-if-then:

Merge If Then
+++++++++++++

.. meta::
	:description:
		Merge If Then: Two nested if/then may be merged into one, by merging the two conditions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Merge If Then
	:twitter:description: Merge If Then: Two nested if/then may be merged into one, by merging the two conditions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Merge If Then
	:og:type: article
	:og:description: Two nested if/then may be merged into one, by merging the two conditions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/MergeIfThen.html
	:og:locale: en
Two nested if/then may be merged into one, by merging the two conditions. This is often a development artifact. 

.. code-block:: php
   
   <?php
   
   // two merged conditions
   if ($a == 1 && $b == 2) {
       // doSomething()
   }
   
   // two distinct conditions
   // two nesting
   if ($a == 1) {
       if ($b == 2) {
           // doSomething()
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `if-then <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Suggestions
___________

* Merge the two structures into one




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MergeIfThen                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
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


