.. _classes-toomanychildren:

.. _too-many-children:

Too Many Children
+++++++++++++++++

.. meta::
	:description:
		Too Many Children: Classes that have more than 15 children.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Many Children
	:twitter:description: Too Many Children: Classes that have more than 15 children
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Many Children
	:og:type: article
	:og:description: Classes that have more than 15 children
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Too Many Children.html
	:og:locale: en
Classes that have more than 15 children. It is worth checking if they cannot be refactored in anyway.

The threshold of 15 children can be configured. There is no technical limitation of the number of children and grand-children for a class. 

The analysis doesn't work recursively : only direct generations are counted. Only children that can be found in the code are counted.

.. code-block:: php
   
   <?php
   
   // parent class
   // calling it grandparent to avoid confusion with 'parent'
   class grandparent {}
   
   
   class children1 extends grandparent {}
   class children2 extends grandparent {}
   class children3 extends grandparent {}
   class children4 extends grandparent {}
   class children5 extends grandparent {}
   class children6 extends grandparent {}
   class children7 extends grandparent {}
   class children8 extends grandparent {}
   class children9 extends grandparent {}
   class children11 extends grandparent {}
   class children12 extends grandparent {}
   class children13 extends grandparent {}
   class children14 extends grandparent {}
   class children15 extends grandparent {}
   class children16 extends grandparent {}
   class children17 extends grandparent {}
   class children18 extends grandparent {}
   class children19 extends grandparent {}
   
   ?>

+--------------------+---------+---------+--------------------------------------------------------+
| Name               | Default | Type    | Description                                            |
+--------------------+---------+---------+--------------------------------------------------------+
| childrenClassCount | 15      | integer | Threshold for too many children classes for one class. |
+--------------------+---------+---------+--------------------------------------------------------+



See also `Why is subclassing too much bad (and hence why should we use prototypes to do away with it)? <https://softwareengineering.stackexchange.com/questions/137687/why-is-subclassing-too-much-bad-and-hence-why-should-we-use-prototypes-to-do-aw>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_


Suggestions
___________

* Split the original class into more specialised classes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/TooManyChildren                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-typo3-classes-toomanychildren`, :ref:`case-woocommerce-classes-toomanychildren`                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


