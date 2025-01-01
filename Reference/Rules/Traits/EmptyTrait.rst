.. _traits-emptytrait:

.. _empty-traits:

Empty Traits
++++++++++++

.. meta::
	:description:
		Empty Traits: List of all empty trait defined in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Traits
	:twitter:description: Empty Traits: List of all empty trait defined in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Traits
	:og:type: article
	:og:description: List of all empty trait defined in the code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Traits/EmptyTrait.html
	:og:locale: en
List of all empty trait defined in the code. 



Such traits may be reserved for future use. They may also be forgotten, and dead code.

.. code-block:: php
   
   <?php
   
   // empty trait
   trait t { }
   
   // Another empty trait
   trait t2 {
       use t; 
   }
   
   ?>
Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Suggestions
___________

* Add some code to the trait
* Remove the trait




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/EmptyTrait                                                                                                                                    |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


