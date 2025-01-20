.. _type-gpcindex:

.. _incoming-variable-index-inventory:

Incoming Variable Index Inventory
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Incoming Variable Index Inventory: This rule collects all the index used in incoming variables : ``$_GET``, ``$_POST``, ``$_REQUEST``, ``$_COOKIE``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Incoming Variable Index Inventory
	:twitter:description: Incoming Variable Index Inventory: This rule collects all the index used in incoming variables : ``$_GET``, ``$_POST``, ``$_REQUEST``, ``$_COOKIE``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Incoming Variable Index Inventory
	:og:type: article
	:og:description: This rule collects all the index used in incoming variables : ``$_GET``, ``$_POST``, ``$_REQUEST``, ``$_COOKIE``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Incoming Variable Index Inventory.html
	:og:locale: en
This rule collects all the index used in incoming variables : ``$_GET``, ``$_POST``, ``$_REQUEST``, ``$_COOKIE``. 

Collecting together the names of incoming variable is good for documentation.


.. code-block:: php
   
   <?php
   
   // x is collected
   echo $_GET['x'];
   
   // y is collected, but no z. 
   echo $_POST['y']['z'];
   
   // s is not collected
   echo $_ENV['s'];
   
   ?>
Connex PHP features
-------------------

  + `super-global <https://php-dictionary.readthedocs.io/en/latest/dictionary/super-global.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/GPCIndex                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                                                                   |
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


