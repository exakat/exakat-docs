.. _php-firstclasscallable:

.. _first-class-callable:

First Class Callable
++++++++++++++++++++

.. meta::
	:description:
		First Class Callable: A syntax using ellipsis was introduced to make it easy to make a method into a callable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: First Class Callable
	:twitter:description: First Class Callable: A syntax using ellipsis was introduced to make it easy to make a method into a callable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: First Class Callable
	:og:type: article
	:og:description: A syntax using ellipsis was introduced to make it easy to make a method into a callable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/First Class Callable.html
	:og:locale: en
A syntax using ellipsis was introduced to make it easy to make a method into a callable.

.. code-block:: php
   
   <?php
   
   // Using ellipsis as the only argument
   $a = $object->method(...);
   
   // Old style equivalent
   $a = array($object, 'method');
   
   // calling the closure.
   $a();
   
   ?>

See also `PHP RFC: First-class callable syntax <https://wiki.php.net/rfc/first_class_callable_syntax>`_.

Connex PHP features
-------------------

  + `first-class-callable <https://php-dictionary.readthedocs.io/en/latest/dictionary/first-class-callable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/FirstClassCallable                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


