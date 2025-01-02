.. _classes-citsamename:

.. _class,-interface,-enum-or-trait-with-identical-names:

Class, Interface, Enum Or Trait With Identical Names
++++++++++++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Class, Interface, Enum Or Trait With Identical Names: The following names are used at the same time for classes, interfaces or traits.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class, Interface, Enum Or Trait With Identical Names
	:twitter:description: Class, Interface, Enum Or Trait With Identical Names: The following names are used at the same time for classes, interfaces or traits
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class, Interface, Enum Or Trait With Identical Names
	:og:type: article
	:og:description: The following names are used at the same time for classes, interfaces or traits
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class, Interface, Enum Or Trait With Identical Names.html
	:og:locale: en
The following names are used at the same time for classes, interfaces or traits. For example, 
Even if they are in different namespaces, identical names makes classes easy to confuse. This is often solved by using alias at import time : this leads to more confusion, as a class suddenly changes its name. 

Internally, PHP use the same list for all classes, interfaces and traits. As such, it is not allowed to have both a trait and a class with the same name.

In PHP 4, and PHP 5 before namespaces, it was not possible to have classes with the same name. They were simply included after a check.

.. code-block:: php
   
   <?php
       class a     { /* some definitions */ }
       interface a { /* some definitions */ }
       trait a     { /* some definitions */ }
       enum a      { /* some definitions */ } // PHP 8.1
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Use distinct names for every class, trait and interface. 
* Keep eponymous classes, traits and interfaces in distinct files, for definition but also for usage. When this happens, rename one of them.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CitSameName                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-classes-citsamename`, :ref:`case-nextcloud-classes-citsamename`                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


