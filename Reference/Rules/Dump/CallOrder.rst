.. _dump-callorder:

.. _call-order:

Call Order
++++++++++

.. meta::
	:description:
		Call Order: This is a representation of the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Call Order
	:twitter:description: Call Order: This is a representation of the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Call Order
	:og:type: article
	:og:description: This is a representation of the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Call Order.html
	:og:locale: en
This is a representation of the code. Each node is a function or method, and each link a is call from a method to another.

The only link is the possible call from a method to the other. All control flow is omitted, including conditional calls and loops.
From the above script, the resulting network will display 'foo() -> bar(), foo() -> foobar(), bar() -> foobar()' calls.

.. code-block:: php
   
   <?php
       
       function foo() {
           bar();
           foobar();
       }
       
       function bar() {
           foobar();
       }
       
       function foobar() {
       
       }
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CallOrder                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                                                                                   |
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


