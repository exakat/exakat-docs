.. _psr-psr13usage:

.. _psr-13-usage:

PSR-13 Usage
++++++++++++

.. meta::
	:description:
		PSR-13 Usage: PSR-13 describes a common interface for dependency injection containers.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PSR-13 Usage
	:twitter:description: PSR-13 Usage: PSR-13 describes a common interface for dependency injection containers
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PSR-13 Usage
	:og:type: article
	:og:description: PSR-13 describes a common interface for dependency injection containers
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PSR-13 Usage.html
	:og:locale: en
PSR-13 describes a common interface for dependency injection containers.

It is supported by an set of interfaces, that one may use in the code.

.. code-block:: php
   
   <?php
   
   namespace MyNamespace;
   
   // MyLink implements the PSR-13 LinkInterface.
   // MyLink is more of a black hole than a real Container.
   class MyLink implements LinkInterface {
       public function getHref() {}
       public function isTemplated() {}
       public function getRels() {}
       public function getAttributes() {}
   }
   
   ?>

See also `PSR-13 : Link definition interface <http://www.php-fig.org/psr/psr-13/>`_.

Connex PHP features
-------------------

  + `psr <https://php-dictionary.readthedocs.io/en/latest/dictionary/psr.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Psr/Psr13Usage                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                                                                                  |
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


