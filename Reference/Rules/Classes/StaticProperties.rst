.. _classes-staticproperties:

.. _static-properties:

Static Properties
+++++++++++++++++

.. meta\:\:
	:description:
		Static Properties: List of all static properties.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Properties
	:twitter:description: Static Properties: List of all static properties
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Properties
	:og:type: article
	:og:description: List of all static properties
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/StaticProperties.html
	:og:locale: en
  List of all `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties.

.. code-block:: php
   
   <?php
   
   class foo {
       static public $staticProperty = 1;
              public $notStaticProperty = 2;
              
       private function method() {
           // This is not a property
           new static();
       }
   }
   
   function bar() {
       // This is not a static property
       static $staticVariable;
       
       //....
   }
   
   ?>
Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StaticProperties                                                                                                                                                                |
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


