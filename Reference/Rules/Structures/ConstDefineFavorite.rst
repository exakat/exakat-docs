.. _structures-constdefinefavorite:

.. _const-or-define:

Const Or Define
+++++++++++++++

.. meta\:\:
	:description:
		Const Or Define: ``const`` and ``define()`` have the same functional use : create constants.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Const Or Define
	:twitter:description: Const Or Define: ``const`` and ``define()`` have the same functional use : create constants
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Const Or Define
	:og:type: article
	:og:description: ``const`` and ``define()`` have the same functional use : create constants
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ConstDefineFavorite.html
	:og:locale: en
  ``const`` and ``define()`` have the same functional use : create constants. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

They are almost interchangeable, though not totally : ``define()`` allows the creation of case-insensitive constants, while ``Const`` won\'t.

.. code-block:: php
   
   <?php
   
   // be consistent
   const A1  = 1 ;
   const A2  = 2 ;
   const A3  = 3 ;
   const A4  = 4 ;
   const A5  = 5 ;
   const A6  = 6 ;
   const A7  = 7 ;
   const A8  = 8 ;
   const A9  = 9 ;
   const A10 = 10;
   const A11 = 11;
   
   define('A12', 12); // Be consistent, always use the same. 
   
   ?>

See also `define <https://www.php.net/manual/en/function.define.php>`_ and `const <http://www.php.net/manual/en/language.constants.php>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ConstDefineFavorite                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.1                                                                                                                                                                                  |
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


