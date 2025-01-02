.. _complete-setmethodfnp:

.. _set-method-fnp:

Set Method Fnp
++++++++++++++

.. meta::
	:description:
		Set Method Fnp: Complete code by adding the ``fullnspath`` property to methods calls.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Method Fnp
	:twitter:description: Set Method Fnp: Complete code by adding the ``fullnspath`` property to methods calls
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Method Fnp
	:og:type: article
	:og:description: Complete code by adding the ``fullnspath`` property to methods calls
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Set Method Fnp.html
	:og:locale: en
Complete code by adding the ``fullnspath`` property to methods calls. 

It makes it faster to find definitions later.

.. code-block:: php
   
   <?php
   
   function foo(X $a) {
   	// \x::moo 
   	$a->moo();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetMethodFnp                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
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


