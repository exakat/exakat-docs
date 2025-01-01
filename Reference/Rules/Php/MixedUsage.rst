.. _php-mixedusage:

.. _mixed-typehint-usage:

Mixed Typehint Usage
++++++++++++++++++++

.. meta::
	:description:
		Mixed Typehint Usage: Usage of the mixed typehint.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mixed Typehint Usage
	:twitter:description: Mixed Typehint Usage: Usage of the mixed typehint
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mixed Typehint Usage
	:og:type: article
	:og:description: Usage of the mixed typehint
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/MixedUsage.html
	:og:locale: en
Usage of the mixed typehint.

.. code-block:: php
   
   <?php
   
   function foo() : mixed {
       switch(rand(0, 3)) {
           case 0:
               return false;
               
           case 1: 
               return 'a';
               
           case 2:
               return [];
               
           default:
               return null;
       }
   }
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/language.types.declarations.php>`_.

Connex PHP features
-------------------

  + `mixed <https://php-dictionary.readthedocs.io/en/latest/dictionary/mixed.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MixedUsage                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


