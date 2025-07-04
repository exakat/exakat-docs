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

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ComparedButNotAssignedStrings.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ComparedButNotAssignedStrings.html","name":"Compared But Not Assigned Strings","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"The reported strings are compared to variable, or data containers, in the code, but those values are never assigned","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Compared But Not Assigned Strings.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

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

  + `Comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_
  + `Assignations <https://php-dictionary.readthedocs.io/en/latest/dictionary/assignation.ini.html>`_


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


