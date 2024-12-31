.. _complete-overwrittenmethods:

.. _overwritten-methods:

Overwritten Methods
+++++++++++++++++++

.. meta\:\:
	:description:
		Overwritten Methods: This command adds OVERWRITE link between methods definitions of classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwritten Methods
	:twitter:description: Overwritten Methods: This command adds OVERWRITE link between methods definitions of classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwritten Methods
	:og:type: article
	:og:description: This command adds OVERWRITE link between methods definitions of classes
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/OverwrittenMethods.html
	:og:locale: en
  This command adds OVERWRITE link between methods definitions of classes.



The `foo` method will be linked between classes x and y, with an OVERWRITE link.

.. code-block:: php
   
   <?php
   
   class x {
       protected function foo() {}
   }
   
   class y extends x {
       protected function foo() {}
   }
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_
  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/OverwrittenMethods                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
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


