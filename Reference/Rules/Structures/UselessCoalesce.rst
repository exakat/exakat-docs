.. _structures-uselesscoalesce:

.. _useless-coalesce:

Useless Coalesce
++++++++++++++++

.. meta::
	:description:
		Useless Coalesce: The .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Coalesce
	:twitter:description: Useless Coalesce: The 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Coalesce
	:og:type: article
	:og:description: The 
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Coalesce.html
	:og:locale: en
The ?: operator needs the condition to be potentially empty. This means that the type should have the possibility to be null, false, 0, or any of the empty values.

.. code-block:: php
   
   <?php
   
   function foo(A $a, bool $b) {
   	$a ?: 'a';
   	$b ?: 'a';
   }
   
   ?>

Suggestions
___________

* Remove the operator.
* Extend the type to include values that may be empty.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessCoalesce                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


