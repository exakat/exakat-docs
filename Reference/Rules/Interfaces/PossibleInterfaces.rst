.. _interfaces-possibleinterfaces:

.. _possible-interfaces:

Possible Interfaces
+++++++++++++++++++

.. meta::
	:description:
		Possible Interfaces: This analyzer lists classes that may be a base to create interfaces.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Possible Interfaces
	:twitter:description: Possible Interfaces: This analyzer lists classes that may be a base to create interfaces
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Possible Interfaces
	:og:type: article
	:og:description: This analyzer lists classes that may be a base to create interfaces
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Possible Interfaces.html
	:og:locale: en
This analyzer lists classes that may be a base to create interfaces. 

Currently, classes with more than 1 defined method are used to identify possible interfaces. An interfaces are considered when at least 2 methods are common in 3 classes.

Only the name of the method is used to identify possible methods. Signature and method options are not taken into account.

.. code-block:: php
   
   <?php
   
   class a {
       function m1 () {}
       function m2 () {}
       function m3 () {}
   }
   
   class b {
       function m1 () {}
       function m2 () {}
       function m4 () {}
   }
   
   // This class has not enough shared methods with other classes
   class c {
       function m1 () {}
       function m4 () {}
       function m5 () {}
   }
   
   ?>
Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Add those interfaces, and use the `implements` keyword in the mentioned classes.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/PossibleInterfaces                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.6                                                                                                                   |
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


