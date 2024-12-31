.. _dump-neworder:

.. _new-order:

New Order
+++++++++

.. meta\:\:
	:description:
		New Order: Order in which new calls must be called.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Order
	:twitter:description: New Order: Order in which new calls must be called
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Order
	:og:type: article
	:og:description: Order in which new calls must be called
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/NewOrder.html
	:og:locale: en
  Order in which new calls must be called. When a class uses another class type in its constructor, this means the second class must be instantiated before creating the first. This creates an order for classes.

.. code-block:: php
   
   <?php
   
   class x {}
   
   // class Y has precedence over class X, as it needs to be called first to get to X
   class y {
       function foo() {
           return new x();
       }
   }
   
   
   ?>
Connex PHP features
-------------------

  + `new <https://php-dictionary.readthedocs.io/en/latest/dictionary/new.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/NewOrder                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


