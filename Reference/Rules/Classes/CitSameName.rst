.. _classes-citsamename:

.. _class,-interface,-enum-or-trait-with-identical-names:

Class, Interface, Enum Or Trait With Identical Names
++++++++++++++++++++++++++++++++++++++++++++++++++++

  The following names are used at the same time for classes, interfaces or traits. For example, 


.. code-block:: php
   
   <?php
       class a     { /* some definitions */ }
       interface a { /* some definitions */ }
       trait a     { /* some definitions */ }
       enum a      { /* some definitions */ } // PHP 8.1
   ?>


Even if they are in different namespaces, identical names makes classes easy to confuse. This is often solved by using alias at import time : this leads to more confusion, as a class suddenly changes its name. 

Internally, PHP use the same list for all classes, interfaces and traits. As such, it is not allowed to have both a trait and a class with the same name.

In PHP 4, and PHP 5 before namespaces, it was not possible to have classes with the same name. They were simply included after a check.

Suggestions
___________

* Use distinct names for every class, trait and interface. 
* Keep eponymous classes, traits and interfaces in distinct files, for definition but also for usage. When this happens, rename one of them.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CitSameName                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
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
| Features     | class                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-classes-citsamename`, :ref:`case-nextcloud-classes-citsamename`                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


