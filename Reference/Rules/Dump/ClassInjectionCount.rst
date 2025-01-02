.. _dump-classinjectioncount:

.. _class-injection-count:

Class Injection Count
+++++++++++++++++++++

.. meta::
	:description:
		Class Injection Count: Counts the number of arguments in the constructor.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Injection Count
	:twitter:description: Class Injection Count: Counts the number of arguments in the constructor
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Injection Count
	:og:type: article
	:og:description: Counts the number of arguments in the constructor
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class Injection Count.html
	:og:locale: en
Counts the number of arguments in the constructor. Variadic arguments are counted as one. The more injections in a constructor, the harder it is to use it. Although, the threshold for difficulty is probably quite high.

.. code-block:: php
   
   <?php
   
   class x {
   	function __constructor(A $a, B, $b) {
   	
   	}
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/ClassInjectionCount                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


