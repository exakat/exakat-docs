.. _classes-constantdefinition:

.. _constant-definition:

Constant Definition
+++++++++++++++++++

.. meta::
	:description:
		Constant Definition: List of class constants being defined.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Definition
	:twitter:description: Constant Definition: List of class constants being defined
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Definition
	:og:type: article
	:og:description: List of class constants being defined
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constant Definition.html
	:og:locale: en
List of class constants being defined.

.. code-block:: php
   
   <?php
   
   // traditional way of making constants
   define('aConstant', 1);
   
   // modern way of making constants
   const anotherConstant = 2;
   
   class foo {
       // Not a constant, a class constant.
       const aClassConstant = 3;
   }
   
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_ and `PHP OOP Constants <https://tutorials.supunkavinda.blog/php/oop-constants>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ConstantDefinition                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


