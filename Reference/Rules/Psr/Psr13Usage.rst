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
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Psr\/Psr13Usage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Psr\/Psr13Usage.html","name":"PSR-13 Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PSR-13 describes a common interface for dependency injection containers","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PSR-13 Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>PSR-13 describes a common interface for dependency injection containers.

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


