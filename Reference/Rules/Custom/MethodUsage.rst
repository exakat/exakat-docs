.. _custom-methodusage:

.. _method-usage:

Method Usage
++++++++++++

.. meta\:\:
	:description:
		Method Usage: This rule reports method usages.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Usage
	:twitter:description: Method Usage: This rule reports method usages
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Usage
	:og:type: article
	:og:description: This rule reports method usages
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Custom/MethodUsage.html
	:og:locale: en
  This rule reports method usages. The methods that are monitored are set with the parameter ``searchFor``.

.. code-block:: php
   
   <?php
   
   // searchFor = \X::foo
   function bar(X $arg) {
   	$arg->foo();
   }
   
   ?>

+-----------+---------+--------+------------------------------------------------------------------------------------------------+
| Name      | Default | Type   | Description                                                                                    |
+-----------+---------+--------+------------------------------------------------------------------------------------------------+
| searchFor |         | string | Method to report in the codes : use static syntax to describe them : \a::foo(); \a\b\c::goo(). |
+-----------+---------+--------+------------------------------------------------------------------------------------------------+



Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Custom/MethodUsage                                                                                                      |
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
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


