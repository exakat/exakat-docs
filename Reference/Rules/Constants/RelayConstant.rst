.. _constants-relayconstant:

.. _relay-constant:

Relay Constant
++++++++++++++

.. meta::
	:description:
		Relay Constant: A relay constant is a constant that gives another name to an existing constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Relay Constant
	:twitter:description: Relay Constant: A relay constant is a constant that gives another name to an existing constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Relay Constant
	:og:type: article
	:og:description: A relay constant is a constant that gives another name to an existing constant
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Constants/RelayConstant.html
	:og:locale: en
A relay constant is a constant that gives another name to an existing constant. It is simply build by giving the value of another constant.

Relay constants acts as alias. They also add an extra layer between a constant or a literal and its usage.

.. code-block:: php
   
   <?php
   
   class A {
   	const A = 1;
   }
   
   class B {
   	// this constant is actually the A::A constant 
   	const B = A::A;
   }
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/RelayConstant                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.7                                                                                                                   |
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


