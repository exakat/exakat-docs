.. _psr-psr3usage:

.. _psr-3-usage:

PSR-3 Usage
+++++++++++

.. meta::
	:description:
		PSR-3 Usage: PSR-3 describes a common interface for logging libraries.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PSR-3 Usage
	:twitter:description: PSR-3 Usage: PSR-3 describes a common interface for logging libraries
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PSR-3 Usage
	:og:type: article
	:og:description: PSR-3 describes a common interface for logging libraries
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PSR-3 Usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Psr\/Psr3Usage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Psr\/Psr3Usage.html","name":"PSR-3 Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PSR-3 describes a common interface for logging libraries","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PSR-3 Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>PSR-3 describes a common interface for logging libraries.

It is supported by an set of interfaces, that one may use in the code.

.. code-block:: php
   
   <?php
   
   namespace MyNamespace;
   
   // MyLog implements the PSR-3 LoggerInterface.
   // MyLog is more of a black hole than a real Log.
   namespace ;
   
   class MyLog implements \Psr\Log\LoggerInterface {
       public function emergency($message, array $context = array()) {}
       public function alert($message, array $context = array()) {}
       public function critical($message, array $context = array()) {}
       public function error($message, array $context = array()) {}
       public function warning($message, array $context = array()) {}
       public function notice($message, array $context = array()) {}
       public function info($message, array $context = array()) {}
       public function debug($message, array $context = array()) {}
       public function log($level, $message, array $context = array()) {}
   }
   
   ?>

See also `PSR-3 : Logger Interface <http://www.php-fig.org/psr/psr-3/>`_.

Connex PHP features
-------------------

  + `psr <https://php-dictionary.readthedocs.io/en/latest/dictionary/psr.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Psr/Psr3Usage                                                                                                                                                                           |
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


