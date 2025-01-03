.. _typehints-couldberesource:

Typehints/CouldBeResource
+++++++++++++++++++++++++

.. meta::
	:description:
		Typehints/CouldBeResource: Mark arguments, properties and return types that can be set to ``resource``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Typehints/CouldBeResource
	:twitter:description: Typehints/CouldBeResource: Mark arguments, properties and return types that can be set to ``resource``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Typehints/CouldBeResource
	:og:type: article
	:og:description: Mark arguments, properties and return types that can be set to ``resource``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Typehints/CouldBeResource.html
	:og:locale: en
Mark arguments, properties and return types that can be set to ``resource``. 

``resource`` is an internal PHP type, and it should be a scalar type, yet it is not implement yet (as of PHP 8.2). It is still used as such by Exakat.

.. code-block:: php
   
   <?php
   
   class x {
       // $p holds a resource
       private $p;
       
       function __construct() {
           $this->p = fopen('/tmp/file.txt', 'w+');
       }
   }
   ?>
Connex PHP features
-------------------

  + `resource <https://php-dictionary.readthedocs.io/en/latest/dictionary/resource.ini.html>`_
  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeResource                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


