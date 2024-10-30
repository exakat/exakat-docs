.. _psr-psr6usage:

.. _psr-6-usage:

PSR-6 Usage
+++++++++++

  PSR-6 is the cache standard for PHP.

The goal of PSR-6 is to allow developers to create cache-aware libraries that can be integrated into existing frameworks and systems without the need for custom development.

It is supported by an set of interfaces, that one may use in the code.

.. code-block:: php
   
   <?php
   
   namespace MyNamespace;
   
   // MyCacheItem implements the PSR-7 CacheItemInterface.
   // This MyCacheItem is more of a black hole than a real CacheItem.
   class MyCacheItem implements \Psr\Cache\CacheItemInterface {
       public function getKey() {}
       public function get() {}
       public function isHit() {}
       public function set($value) {}
       public function expiresAt($expiration) {}
       public function expiresAfter($time) {}
   }
   
   ?>

See also `PSR-6 : Caching <http://www.php-fig.org/psr/psr-6/>`_.

Connex PHP features
-------------------

  + `psr <https://php-dictionary.readthedocs.io/en/latest/dictionary/psr.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Psr/Psr6Usage                                                                                                                                                                           |
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


