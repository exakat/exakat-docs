.. _type-stringwithstrangespace:

.. _strings-with-strange-space:

Strings With Strange Space
++++++++++++++++++++++++++

  An invisible space may be mistaken for a normal space. 

However, PHP does straight comparisons, and may fail at recognizing. This analysis reports when it finds such strange spaces inside strings.

PHP doesn't mistake space and tables for whitespace when tokenizing the code.

This analysis doesn't report Unicode Codepoint Notation : those are visible in the code.

.. code-block:: php
   
   <?php
   
   // PHP 7 notation, 
   $a = "\u{3000}";
   $b = " ";
   
   // Displays false
   var_dump($a === $b);
   
   ?>

See also `Unicode spaces <https://www.cs.tut.fi/~jkorpela/chars/spaces.html>`_ and `disallow irregular whitespace (no-irregular-whitespace) <http://eslint.org/docs/rules/no-irregular-whitespace>`_.


Suggestions
___________

* Replace the odd spaces with a normal space
* If unsecable spaces are important for presentation, add them at the templating level.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/StringWithStrangeSpace                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.0                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | non-breakable-space                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-type-stringwithstrangespace`, :ref:`case-thelia-type-stringwithstrangespace`                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


