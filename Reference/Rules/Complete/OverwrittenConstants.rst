.. _complete-overwrittenconstants:

.. _overwritten-constant:

Overwritten Constant
++++++++++++++++++++

.. meta::
	:description:
		Overwritten Constant: This command adds OVERWRITE link between class constant definitions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwritten Constant
	:twitter:description: Overwritten Constant: This command adds OVERWRITE link between class constant definitions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwritten Constant
	:og:type: article
	:og:description: This command adds OVERWRITE link between class constant definitions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overwritten Constant.html
	:og:locale: en
This command adds OVERWRITE link between class constant definitions.

A constant is overwritten by another when it is defined in one of the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class or `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ interface.

The `A` constant will be linked between classes x and y, with an OVERWRITE link.

.. code-block:: php
   
   <?php
   
   class x {
       protected const A = 1;
   }
   
   class y extends x {
       protected const A = 1;
   }
   
   ?>
Connex PHP features
-------------------

  + `inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_
  + `final <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_
  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/OverwrittenConstants                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
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


