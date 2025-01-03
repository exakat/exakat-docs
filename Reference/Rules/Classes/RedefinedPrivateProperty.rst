.. _classes-redefinedprivateproperty:

.. _redefined-private-property:

Redefined Private Property
++++++++++++++++++++++++++

.. meta::
	:description:
		Redefined Private Property: Private properties are local to their defined class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Redefined Private Property
	:twitter:description: Redefined Private Property: Private properties are local to their defined class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Redefined Private Property
	:og:type: article
	:og:description: Private properties are local to their defined class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Redefined Private Property.html
	:og:locale: en
Private properties are local to their defined class. PHP doesn't forbid the re-declaration of a private property in a child class.

However, having two or more properties with the same name, in the class hierarchy tends to be `error <https://www.php.net/error>`_ prone. Methods will be accessing properties with the same name, but with different values.

.. code-block:: php
   
   <?php
   
   class A {
       private $isReady = true;
   }
   
   class B {
       private $isReady = false;
   }
   
   ?>
Connex PHP features
-------------------

  + `private <https://php-dictionary.readthedocs.io/en/latest/dictionary/private.ini.html>`_


Suggestions
___________

* Remove the property in the children classes
* Rename the property in the children classes
* Change the visibility in the parent class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/RedefinedPrivateProperty                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-classes-redefinedprivateproperty`                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


