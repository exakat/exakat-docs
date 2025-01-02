.. _php-useweb:

.. _use-web:

Use Web
+++++++

.. meta::
	:description:
		Use Web: The code is used in web environment.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Web
	:twitter:description: Use Web: The code is used in web environment
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Web
	:og:type: article
	:og:description: The code is used in web environment
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Web.html
	:og:locale: en
The code is used in web environment.

The web environement is identified through the usage of the superglobals: ``$_GET``, ``$_POST``, etc.

.. code-block:: php
   
   <?php
   
   // Accessing $_GET is possible when PHP is used in a web server.
   $x = filter_validate($_GET['x'], FILTER_EMAIL);
   
   ?>
Connex PHP features
-------------------

  + `web <https://php-dictionary.readthedocs.io/en/latest/dictionary/web.ini.html>`_
  + `superglobal <https://php-dictionary.readthedocs.io/en/latest/dictionary/superglobal.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseWeb                                                                                                                                                                              |
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


