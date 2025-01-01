.. _classes-isupperfamily:

.. _is-upper-family:

Is Upper Family
+++++++++++++++

.. meta::
	:description:
		Is Upper Family: Does the static call is made within the current hierarchy of class, or, is it made in the class, in the children or outside.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is Upper Family
	:twitter:description: Is Upper Family: Does the static call is made within the current hierarchy of class, or, is it made in the class, in the children or outside
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is Upper Family
	:og:type: article
	:og:description: Does the static call is made within the current hierarchy of class, or, is it made in the class, in the children or outside
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/IsUpperFamily.html
	:og:locale: en
Does the `static <https://www.php.net/manual/en/language.oop5.static.php>`_ call is made within the current hierarchy of class, or, is it made in the class, in the children or outside. 

This applies to `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methodcalls, property accesses and class constants.

.. code-block:: php
   
   <?php
   
   class AAA            { function inAAA() {} }   // upper family : grand-parent
   class AA extends AAA { function inAA()  {} }   // upper family : parent
   class A  extends AA  { function inA()  {} }    // current family
   class B  extends A   { function inB()  {} }    // lower family
   class C              { function inC()  {} }    // outside family
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IsUpperFamily                                                                                                   |
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


