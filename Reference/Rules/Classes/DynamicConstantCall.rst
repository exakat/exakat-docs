.. _classes-dynamicconstantcall:

.. _dynamic-class-constant:

Dynamic Class Constant
++++++++++++++++++++++

.. meta::
	:description:
		Dynamic Class Constant: This is the list of dynamic calls to class constants.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Class Constant
	:twitter:description: Dynamic Class Constant: This is the list of dynamic calls to class constants
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Class Constant
	:og:type: article
	:og:description: This is the list of dynamic calls to class constants
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamic Class Constant.html
	:og:locale: en
This is the list of dynamic calls to class constants.

Constant may be dynamically called with the `constant() <https://www.php.net/constant>`_ function. In PHP 8.3, they may also be called with a new dedicated syntax. 

.. code-block:: php
   
   <?php
       // Dynamic access to 'E_ALL'
       echo constant('E_ALL');
       
       interface i {
           const MY_CONSTANT  = 1;
       }
   
       // Dynamic access to 'E_ALL'
       $constantName = 'MY_CONSTANT';
       echo constant('i::'.$constantName);
   
       // With PHP 8.3 : 
       echo i::{$constantName};
   
   ?>
Connex PHP features
-------------------

  + `dynamic-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicConstantCall                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


