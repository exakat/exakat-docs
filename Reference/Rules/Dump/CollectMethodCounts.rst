.. _dump-collectmethodcounts:

.. _collect-method-counts:

Collect Method Counts
+++++++++++++++++++++

.. meta::
	:description:
		Collect Method Counts: This analysis collects the number of methods per class, trait or interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Method Counts
	:twitter:description: Collect Method Counts: This analysis collects the number of methods per class, trait or interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Method Counts
	:og:type: article
	:og:description: This analysis collects the number of methods per class, trait or interface
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Dump/CollectMethodCounts.html
	:og:locale: en
This analysis collects the number of methods per class, trait or interface. 

The count applies to classes, anonymous classes, traits and interfaces. They are considered distinct one from another.

.. code-block:: php
   
   <?php
   
   class foo {
       // 2 methods
       function __construct() {}
       function foo() {}
   }
   
   interface bar {
       // 1 method
       function a() ;
   }
   
   class barbar {
       // 3 methods
       function __construct() {}
       function foo() {}
       function a() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectMethodCounts                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                                                   |
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


