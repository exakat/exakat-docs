.. _dump-combinedcalls:

.. _combined-calls:

Combined Calls
++++++++++++++

.. meta::
	:description:
		Combined Calls: This collects all the combined function or method calls.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Combined Calls
	:twitter:description: Combined Calls: This collects all the combined function or method calls
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Combined Calls
	:og:type: article
	:og:description: This collects all the combined function or method calls
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Combined Calls.html
	:og:locale: en
This collects all the combined function or method calls. Those are methods that are called in succession.

.. code-block:: php
   
   <?php
   
   $a = ucfirst(strtolower($name));
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CombinedCalls                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.5                                                                                                                   |
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


