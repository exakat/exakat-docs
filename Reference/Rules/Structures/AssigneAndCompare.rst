.. _structures-assigneandcompare:

.. _assign-and-compare:

Assign And Compare
++++++++++++++++++

.. meta::
	:description:
		Assign And Compare: Assignation has a lower precedence than comparison.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Assign And Compare
	:twitter:description: Assign And Compare: Assignation has a lower precedence than comparison
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Assign And Compare
	:og:type: article
	:og:description: Assignation has a lower precedence than comparison
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Assign And Compare.html
	:og:locale: en
Assignation has a lower precedence than comparison. As such, the assignation always happens after the comparison. This leads to the comparison being stored in the variable, and not the value being compared.

.. code-block:: php
   
   <?php
   
   if ($id = strpos($string, $needle) !== false) { 
       // $id now contains a boolean (true or false), but not the position of the $needle.
   }
   
   // probably valid comparison, as $found will end up being a boolean
   if ($found = strpos($string, $needle) === false) { 
       doSomething();
   }
   
   // always valid comparison, with parenthesis
   if (($id = strpos($string, $needle)) !== false) { 
       // $id now contains a boolean (true or false), but not the position of the $needle.
   }
   
   // Being a lone instruction, this is always valid : there is no double usage with if condition
   $isFound = strpos($string, $needle) !== false;
   
   
   ?>

See also `Operator Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `assignation <https://php-dictionary.readthedocs.io/en/latest/dictionary/assignation.ini.html>`_
  + `comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_


Suggestions
___________

* Use parenthesis
* Separate assignation and comparison
* Drop assignation or comparison




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/AssigneAndCompare                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.3                                                                                                                                                                                   |
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


