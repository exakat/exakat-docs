.. _classes-redefinedmethods:

.. _redefined-methods:

Redefined Methods
+++++++++++++++++

.. meta::
	:description:
		Redefined Methods: Redefined methods are overwritten methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Redefined Methods
	:twitter:description: Redefined Methods: Redefined methods are overwritten methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Redefined Methods
	:og:type: article
	:og:description: Redefined methods are overwritten methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Redefined Methods.html
	:og:locale: en
Redefined methods are overwritten methods. Those methods are defined in different classes that are part of the same classes hierarchy.

Protected and public redefined methods replace each other. Private methods are kept separated, and depends on the caller to be distinguished.

.. code-block:: php
   
   <?php
   
   class foo {
       function method() {
           return 1;
       }
   }
   
   class bar extends foo {
       function method() {
           return 2;
       }
   }
   ?>

See also `Object Inheritance <https://www.php.net/manual/en/language.oop5.inheritance.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/RedefinedMethods                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


