.. _structures-shoulduseexplodeargs:

.. _should-use-explode-args:

Should Use Explode Args
+++++++++++++++++++++++

.. meta::
	:description:
		Should Use Explode Args: explode() has a third argument, which limits the amount of exploded elements.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Explode Args
	:twitter:description: Should Use Explode Args: explode() has a third argument, which limits the amount of exploded elements
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Explode Args
	:og:type: article
	:og:description: explode() has a third argument, which limits the amount of exploded elements
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use Explode Args.html
	:og:locale: en
`explode() <https://www.php.net/explode>`_ has a third argument, which limits the amount of exploded elements. With it, it is possible to collect only the first elements, or drop the last ones.

.. code-block:: php
   
   <?php
   
   $exploded = explode(DELIMITER, $string);
   
   // use explode(DELIMITER, $string, -1);
   array_pop($exploded);
   
   // use explode(DELIMITER, $string, -2);
   $c = array_slice($exploded, 0, -2);
   
   // with explode()'s third argument : 
   list($a, $b) = explode(DELIMITER, $string, 2);
   
   // with list() omitted arguments
   list($a, $b, ) = explode(DELIMITER, $string);
   
   ?>

See also `explode <https://www.php.net/manual/en/function.explode.php>`_.


Suggestions
___________

* Add the third argument to the explode() call




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldUseExplodeArgs                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                                                                                   |
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


