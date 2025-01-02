.. _classes-propertyusedabove:

.. _property-used-above:

Property Used Above
+++++++++++++++++++

.. meta::
	:description:
		Property Used Above: Property used in the parent classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Property Used Above
	:twitter:description: Property Used Above: Property used in the parent classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Property Used Above
	:og:type: article
	:og:description: Property used in the parent classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Property Used Above.html
	:og:locale: en
Property used in the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ classes. If the definition of the property is in the child class, then the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ should not know about it and make usage of it.

It may also be used in the current class, or its children, though this is not reported by this analyzer.

.. code-block:: php
   
   <?php
   
   class A {
       public function foo() {
           $this->pb++;
       }
   }
   
   class B extends A {
       protected $pb = 0;       // property     used above
       protected $pb2 = 0;      // property NOT used above
   }
   
   ?>

See also :ref:`Property Used Below <property-used-below>`.

Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_
  + `inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_


Suggestions
___________

* Move the definition of the property to the upper class
* Move the usage of the property to the lower class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PropertyUsedAbove                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


