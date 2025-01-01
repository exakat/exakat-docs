.. _classes-dynamicselfcalls:

.. _dynamic-self-calls:

Dynamic Self Calls
++++++++++++++++++

.. meta::
	:description:
		Dynamic Self Calls: A class that calls itself dynamically.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Self Calls
	:twitter:description: Dynamic Self Calls: A class that calls itself dynamically
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Self Calls
	:og:type: article
	:og:description: A class that calls itself dynamically
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/DynamicSelfCalls.html
	:og:locale: en
A class that calls itself dynamically. This may be property or methods. 

Calling itself dynamically happens when a class is configured to call various properties (container) or methods.  
This rule is mostly useful internally, to side some special situations.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           $f = 'goo';
           return $this->$f();
       }
   
       function goo() {
           return rand(1, 10);
       }
   }
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicSelfCalls                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


