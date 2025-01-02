.. _structures-emptylines:

.. _empty-instructions:

Empty Instructions
++++++++++++++++++

.. meta::
	:description:
		Empty Instructions: Empty instructions are part of the code that have no instructions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Instructions
	:twitter:description: Empty Instructions: Empty instructions are part of the code that have no instructions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Instructions
	:og:type: article
	:og:description: Empty instructions are part of the code that have no instructions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty Instructions.html
	:og:locale: en
Empty instructions are part of the code that have no instructions. 

This may be trailing semi-colon or empty blocks for if-then structures.

Comments that explains the reason of the situation are not taken into account.

.. code-block:: php
   
   <?php
       $condition = 3;;;;
       if ($condition) { } 
   ?>

Suggestions
___________

* Remove the empty lines
* Fill the empty lines




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EmptyLines                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-structures-emptylines`, :ref:`case-thinkphp-structures-emptylines`                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


