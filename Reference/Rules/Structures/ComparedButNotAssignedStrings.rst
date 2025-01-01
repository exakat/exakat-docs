.. _structures-comparedbutnotassignedstrings:

.. _compared-but-not-assigned-strings:

Compared But Not Assigned Strings
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Compared But Not Assigned Strings: Those strings are compared to variables in the code, but those values are never assigned.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Compared But Not Assigned Strings
	:twitter:description: Compared But Not Assigned Strings: Those strings are compared to variables in the code, but those values are never assigned
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Compared But Not Assigned Strings
	:og:type: article
	:og:description: Those strings are compared to variables in the code, but those values are never assigned
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ComparedButNotAssignedStrings.html
	:og:locale: en
Those strings are compared to variables in the code, but those values are never assigned.

.. code-block:: php
   
   <?php
   
   // some assigned strings in the code
   $a = 'b';
   
   // some compared strings in the code
   // Depending on the origin of $b, is this possible? 
   if ($b === 'c') {
   
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ComparedButNotAssignedStrings                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


