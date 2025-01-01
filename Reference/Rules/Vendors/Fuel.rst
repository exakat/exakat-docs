.. _vendors-fuel:

.. _fuel-php-usage:

Fuel PHP Usage
++++++++++++++

.. meta::
	:description:
		Fuel PHP Usage: This analysis reports usage of the Fuel PHP Framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Fuel PHP Usage
	:twitter:description: Fuel PHP Usage: This analysis reports usage of the Fuel PHP Framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Fuel PHP Usage
	:og:type: article
	:og:description: This analysis reports usage of the Fuel PHP Framework
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Fuel.html
	:og:locale: en
This analysis reports usage of the Fuel PHP Framework. 
Do not confuse fuelPHP and fuelCMS

.. code-block:: php
   
   <?php
   // file located in APPPATH/classes/presenter.php
   class Presenter extends \Fuel\Core\Presenter
   {
       // namespace prefix
       protected static $ns_prefix = 'Presenter\';
   }
   ?>

See also `FuelPHP <https://fuelphp.com>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Fuel                                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


