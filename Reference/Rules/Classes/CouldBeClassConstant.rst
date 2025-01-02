.. _classes-couldbeclassconstant:

.. _could-be-class-constant:

Could Be Class Constant
+++++++++++++++++++++++

.. meta::
	:description:
		Could Be Class Constant: When a property is defined, with a default value, then read, but never modified, it could be turned into a constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Class Constant
	:twitter:description: Could Be Class Constant: When a property is defined, with a default value, then read, but never modified, it could be turned into a constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Class Constant
	:og:type: article
	:og:description: When a property is defined, with a default value, then read, but never modified, it could be turned into a constant
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Class Constant.html
	:og:locale: en
When a property is defined, with a default value, then read, but never modified, it could be turned into a constant. 

Such a property may initially be intended to have a value update, but that never turned out in the code. 

By making the property a constant, it makes visible its constant nature, and reduce the complexity of the code.

.. code-block:: php
   
   <?php
   
   class foo {
       // $this->bar is never modified. 
       private $bar = 1;
       
       // $this->foofoo is modified, at least once
       private $foofoo = 2;
       
       function method($a) {
           $this->foofoo = $this->bar + $a + $this->foofoo;
           
           return $this->foofoo;
       }
       
   }
   
   ?>

See also Class Constants `<https://www.php.net/manual/en/language.oop5.constants.php>`_.

Connex PHP features
-------------------

  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_
  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Turn the property into a class constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeClassConstant                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Class Review <ruleset-Class-Review>`                                                    |
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
| Related rule | :ref:`never-called-parameter`, :ref:`unused-parameter`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


