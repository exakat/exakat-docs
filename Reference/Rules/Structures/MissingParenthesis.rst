.. _structures-missingparenthesis:

.. _missing-parenthesis:

Missing Parenthesis
+++++++++++++++++++

.. meta\:\:
	:description:
		Missing Parenthesis: Adding parenthesis to addition expressions make them more readable and to prevent bugs.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Missing Parenthesis
	:twitter:description: Missing Parenthesis: Adding parenthesis to addition expressions make them more readable and to prevent bugs
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Missing Parenthesis
	:og:type: article
	:og:description: Adding parenthesis to addition expressions make them more readable and to prevent bugs
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/MissingParenthesis.html
	:og:locale: en
  Adding parenthesis to addition expressions make them more readable and to prevent bugs. 

In the expressions below, the code is legit, although it is prone to misunderstanding.

.. code-block:: php
   
   <?php
   
   // Missing some parenthesis!!
   if (!$a instanceof Stdclass) {
       print "Not\n";
   } else {
       print "Is\n";
   }
   
   // Could this addition be actually,
   $c = -$a + $b;
   
   // this one ? 
   $c = -($a + $b);
   
   // or this one ? 
   $c = $b - $a;
   
   ?>

See also `Operators Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `parenthesis <https://php-dictionary.readthedocs.io/en/latest/dictionary/parenthesis.ini.html>`_
  + `readability <https://php-dictionary.readthedocs.io/en/latest/dictionary/readability.ini.html>`_


Suggestions
___________

* Use parenthesis to show intent in the addition expression




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MissingParenthesis                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


