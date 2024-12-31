.. _dump-cyclomaticcomplexity:

.. _cyclomatic-complexity:

Cyclomatic Complexity
+++++++++++++++++++++

.. meta\:\:
	:description:
		Cyclomatic Complexity: This rules calculates cyclomatic complexity for each method, function, and closures.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cyclomatic Complexity
	:twitter:description: Cyclomatic Complexity: This rules calculates cyclomatic complexity for each method, function, and closures
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cyclomatic Complexity
	:og:type: article
	:og:description: This rules calculates cyclomatic complexity for each method, function, and closures
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CyclomaticComplexity.html
	:og:locale: en
  This rules calculates cyclomatic complexity for each method, function, and closures.

.. code-block:: php
   
   <?php
   
   // cyclomatic complexity of 2
   function foo() {
   	if ($a) {
   	
   	} else {
   	
   	}
   }
   
   ?>

See also `Cyclomatic complexity <https://en.wikipedia.org/wiki/Cyclomatic_complexity>`_.

Connex PHP features
-------------------

  + `cyclomatic-complexity <https://php-dictionary.readthedocs.io/en/latest/dictionary/cyclomatic-complexity.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CyclomaticComplexity                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
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


