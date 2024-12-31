.. _classes-cantinstantiatenonclass:

.. _cant-instantiate-non-class:

Cant Instantiate Non Class
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Cant Instantiate Non Class: It is not possible to instantiate anything else than a class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cant Instantiate Non Class
	:twitter:description: Cant Instantiate Non Class: It is not possible to instantiate anything else than a class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cant Instantiate Non Class
	:og:type: article
	:og:description: It is not possible to instantiate anything else than a class
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/CantInstantiateNonClass.html
	:og:locale: en
  It is not possible to instantiate anything else than a class. Interfaces, enumerations and traits cannot be instantiated.

.. code-block:: php
   
   <?php
   
   class c {} 
   
   $object = new c;
   
   trait t {}
   new t;
   
   ?>
Related PHP errors 
-------------------

  + `Cannot instantiate trait %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-instantiate-trait-%25s.html>`_
  + `Cannot instantiate interface %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-instantiate-interface-%25s.html>`_
  + `Cannot instantiate enum %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-instantiate-enum-%25s.html>`_




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantInstantiateNonClass                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
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


