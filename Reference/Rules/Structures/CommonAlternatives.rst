.. _structures-commonalternatives:

.. _common-alternatives:

Common Alternatives
+++++++++++++++++++

.. meta::
	:description:
		Common Alternatives: In the following conditional structures, expressions were found that are common to both 'then' and 'else'.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Common Alternatives
	:twitter:description: Common Alternatives: In the following conditional structures, expressions were found that are common to both 'then' and 'else'
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Common Alternatives
	:og:type: article
	:og:description: In the following conditional structures, expressions were found that are common to both 'then' and 'else'
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/CommonAlternatives.html
	:og:locale: en
In the following conditional structures, expressions were found that are common to both 'then' and 'else'. It may be interesting, though not always possible, to put them both out of the conditional, and reduce line count. 
may be rewritten in :

.. code-block:: php
   
   <?php
   if ($c == 5) {
       $b = strtolower($b[2]); 
       $a++;
   } else {
       $b = strtolower($b[2]); 
       $b++;
   }
   ?>

Suggestions
___________

* Collect common expressions, and move them before of after the if/then expression.
* Move a prefix and suffixes to a third-party method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CommonAlternatives                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolibarr-structures-commonalternatives`, :ref:`case-nextcloud-structures-commonalternatives`                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


