.. _namespaces-shouldmakealias:

.. _should-make-alias:

Should Make Alias
+++++++++++++++++

.. meta\:\:
	:description:
		Should Make Alias: Long names should be aliased.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Make Alias
	:twitter:description: Should Make Alias: Long names should be aliased
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Make Alias
	:og:type: article
	:og:description: Long names should be aliased
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Namespaces/ShouldMakeAlias.html
	:og:locale: en
  Long names should be aliased.

Aliased names are easy to read at the beginning of the script; they may be changed at one point, and update the whole code at the same time. 
Finally, short names makes the rest of the code readable.

.. code-block:: php
   
   <?php
   
   namespace x\y\z;
   
   use a\b\c\d\e\f\g as Object;
   
   // long name, difficult to read, prone to change.
   new a\b\c\d\e\f\g();
   
   // long name, difficult to read, prone to silent dead code if namespace change.
   if ($o instanceof a\b\c\d\e\f\g) {
       
   }
   
   // short names Easy to update all at once.
   new Object();
   if ($o instanceof Object) {
       
   }
   
   ?>

Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/ShouldMakeAlias                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


