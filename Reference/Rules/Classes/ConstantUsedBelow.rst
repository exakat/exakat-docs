.. _classes-constantusedbelow:

.. _constant-used-below:

Constant Used Below
+++++++++++++++++++

.. meta::
	:description:
		Constant Used Below: Mark class constants that are used in children classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Used Below
	:twitter:description: Constant Used Below: Mark class constants that are used in children classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Used Below
	:og:type: article
	:og:description: Mark class constants that are used in children classes
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/ConstantUsedBelow.html
	:og:locale: en
Mark class constants that are used in children classes.
This analysis marks constants at their definition, not the current class, nor the (grand-)`parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

.. code-block:: php
   
   <?php
   
   class foo {
       // This constant is used in children
       protected PROTECTEDPROPERTY = 1;
       
       // This constant is not used in children
       protected LOCALPROTECTEDPROPERTY = 1;
   
       private function foobar() {
           // PROTECTEDPROPERTY is used here, but defined in parent
           echo self::LOCALPROTECTEDPROPERTY;
       }
   }
   
   class foofoo extends foo {
       private function bar() {
           // protectedProperty is used here, but defined in parent
           print self::PROTECTEDPROPERTY;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ConstantUsedBelow                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.10                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


