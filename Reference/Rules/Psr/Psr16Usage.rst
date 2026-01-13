.. _psr-psr16usage:

.. _psr-16-usage:

PSR-16 Usage
++++++++++++

  PSR-16 describes a simple yet extensible interface for a cache item and a cache driver. It is supported by an set of interfaces, that one may use in the code.

.. code-block:: php
   
   <?php
   
   namespace My\SimpleCache;
   
   // MyCache implements the PSR-16 Simple cache.
   // MyCache is more of a black hole than a real cache.
   class MyCache implements Psr\SimpleCache\CacheInterface {
       public function get($key, $default = null) {}
       public function set($key, $value, $ttl = null) {}
       public function delete($key) {}
       public function clear() {}
       public function getMultiple($keys, $default = null) {}
       public function setMultiple($values, $ttl = null) {}
       public function deleteMultiple($keys) {}
       public function has($key) {}
   }
   
   ?>

See also `PSR-16 : Common Interface for Caching Libraries <http://www.php-fig.org/psr/psr-16/>`_.

Connex PHP features
-------------------

  + `psr <https://php-dictionary.readthedocs.io/en/latest/dictionary/psr.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Psr/Psr16Usage                                                                                                                                                                          |
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


