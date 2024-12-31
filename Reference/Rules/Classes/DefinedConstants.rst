.. _classes-definedconstants:

.. _defined-class-constants:

Defined Class Constants
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Defined Class Constants: Checks if class constants are defined.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Defined Class Constants
	:twitter:description: Defined Class Constants: Checks if class constants are defined
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Defined Class Constants
	:og:type: article
	:og:description: Checks if class constants are defined
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/DefinedConstants.html
	:og:locale: en
  Checks if class constants are defined. This includes class constants, one level of `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ (extended) or interfaces (implemented).

This analysis takes into account native PHP, extension and stubs class definitions.

.. code-block:: php
   
   <?php
   
   class X {
       const Y = 2;
       
       function foo() {
           // This is defined on the line above
           echo self::Y;
   
           // This is not defined in the current code
           echo X::X;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DefinedConstants                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


