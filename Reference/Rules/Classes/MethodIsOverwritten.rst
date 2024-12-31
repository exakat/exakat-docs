.. _classes-methodisoverwritten:

.. _method-is-overwritten:

Method Is Overwritten
+++++++++++++++++++++

.. meta\:\:
	:description:
		Method Is Overwritten: This rule marks a method that is overwritten in a child class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Is Overwritten
	:twitter:description: Method Is Overwritten: This rule marks a method that is overwritten in a child class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Is Overwritten
	:og:type: article
	:og:description: This rule marks a method that is overwritten in a child class
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/MethodIsOverwritten.html
	:og:locale: en
  This rule marks a method that is overwritten in a child class. 

Any child that overwrite the method make that method reported here: the `result <https://www.php.net/result>`_ may be partial. 

This rule may lead to the usage of the ``Override`` `attribute <https://www.php.net/attribute>`_.


.. code-block:: php
   
   <?php
   
   class A {
       function intactMethodA() {}         // Not overwritten in any children
       function overwrittenMethodInAA() {} // overwritten in AA
   }
   
   class AA extends A {
       function intactMethodAA() {}        // Not overwritten, because no extends
       function overwrittenMethodInAA() {} // Not overwritten, because no extends
   }
   
   ?>
Connex PHP features
-------------------

  + `inheritance <https://php-dictionary.readthedocs.io/en/latest/dictionary/inheritance.ini.html>`_
  + `override <https://php-dictionary.readthedocs.io/en/latest/dictionary/override.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MethodIsOverwritten                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.9                                                                                                                  |
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


