.. _classes-locallyusedproperty:

.. _locally-used-property:

Locally Used Property
+++++++++++++++++++++

.. meta::
	:description:
		Locally Used Property: List of properties that are used in the class where they are defined.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Locally Used Property
	:twitter:description: Locally Used Property: List of properties that are used in the class where they are defined
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Locally Used Property
	:og:type: article
	:og:description: List of properties that are used in the class where they are defined
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Locally Used Property.html
	:og:locale: en
List of properties that are used in the class where they are defined.

.. code-block:: php
   
   <?php
   
   class foo {
       public $unused, $used;// property $unused is never used in this class
       
       function bar() {
           $this->used++; // property $used is used in this method
       }
   }
   
   $foo = new Foo();
   $foo->unused = 'here'; // property $unused is used outside the class definition
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/LocallyUsedProperty                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


