.. _classes-isextclass:

.. _is-an-extension-class:

Is An Extension Class
+++++++++++++++++++++

.. meta::
	:description:
		Is An Extension Class: Those classes belongs to a PHP Extensions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is An Extension Class
	:twitter:description: Is An Extension Class: Those classes belongs to a PHP Extensions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is An Extension Class
	:og:type: article
	:og:description: Those classes belongs to a PHP Extensions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Is An Extension Class.html
	:og:locale: en
Those classes belongs to a PHP Extensions.

.. code-block:: php
   
   <?php
   
   // This is a native PHP class
   $o = new Stdclass();
   
   // This is not a native PHP class
   $o = new Elephpant();
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `extension <https://php-dictionary.readthedocs.io/en/latest/dictionary/extension.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IsExtClass                                                                                                      |
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


