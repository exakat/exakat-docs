.. _complete-extendedtypehints:

.. _extended-typehints:

Extended Typehints
++++++++++++++++++

.. meta\:\:
	:description:
		Extended Typehints: Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the typehint.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Extended Typehints
	:twitter:description: Extended Typehints: Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the typehint
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Extended Typehints
	:og:type: article
	:og:description: Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the typehint
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/ExtendedTypehints.html
	:og:locale: en
  Produces all the definition links between typehints (arguments, return types, properties) and the definitions that are valid with the typehint.

.. code-block:: php
   
   <?php
   
   function foo(A $A) {}
   
   // This is the raw definition of the above typehint
   interface A {}
   
   // This is valid definition of the above typehint
   class X implements A {}
   // This is valid definition of the above typehint
   class Y extends X {}
   
   // This is not related to the typehint
   class Z {}
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/ExtendedTypehints                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                   |
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


