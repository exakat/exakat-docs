.. _structures-comparedbutnotassignedstrings:

.. _compared-but-not-assigned-strings:

Compared But Not Assigned Strings
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Compared But Not Assigned Strings: The reported strings are compared to variable, or data containers, in the code, but those values are never assigned.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Compared But Not Assigned Strings
	:twitter:description: Compared But Not Assigned Strings: The reported strings are compared to variable, or data containers, in the code, but those values are never assigned
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Compared But Not Assigned Strings
	:og:type: article
	:og:description: The reported strings are compared to variable, or data containers, in the code, but those values are never assigned
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Compared But Not Assigned Strings.html
	:og:locale: en
The reported strings are compared to variable, or data containers, in the code, but those values are never assigned.

It is not possible for the comparison to succeed when no assignation of the value was performed. At least, one variable should be assigned with the value, to be later compared.

It may happen that the value is assigned from an external source, such as a file or a database, and the code does not assign the value explicitly. 


.. code-block:: php
   
   <?php
   
   // some assigned strings in the code
   $a = 'b';
   
   // some compared strings in the code
   // Depending on the origin of $b, is this possible? 
   if ($b === 'c') { }
   
   ?>
Connex PHP features
-------------------

  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_
  + `assignation <https://php-dictionary.readthedocs.io/en/latest/dictionary/assignation.ini.html>`_


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


