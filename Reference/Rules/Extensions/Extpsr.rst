.. _extensions-extpsr:

.. _ext-psr:

ext/psr
+++++++

.. meta::
	:description:
		ext/psr: Extension PSR : PHP Standards Recommendations.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/psr
	:twitter:description: ext/psr: Extension PSR : PHP Standards Recommendations
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/psr
	:og:type: article
	:og:description: Extension PSR : PHP Standards Recommendations
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/psr.html
	:og:locale: en
Extension PSR : PHP Standards Recommendations.

This PHP extension provides the interfaces from the PSR standards as established by the PHP-FIG group. You can use interfaces provided by this extension in another extension easily - see this example.

Currently supported PSR : 

* `PSR-3 <https://www.php-fig.org/psr/psr-3>`_ - `psr/http-message`
* `PSR-11 <https://www.php-fig.org/psr/psr-11>`_ - `psr/container`
* `PSR-13 <https://www.php-fig.org/psr/psr-13>`_ - `psr/link`
* `PSR-15 <https://www.php-fig.org/psr/psr-15>`_ - `psr/http-server`
* `PSR-16 <https://www.php-fig.org/psr/psr-16>`_ - `psr/simple-cache`
* `PSR-17 <https://www.php-fig.org/psr/psr-17>`_ - `psr/http-factory`

.. code-block:: php
   
   <?php
   // Example from the tests, for Cache (PSR-6)
   use Psr\Cache\CacheException;
   class MyCacheException extends Exception implements CacheException {}
   $ex = new MyCacheException('test');
   var_dump($ex instanceof CacheException);
   var_dump($ex instanceof Exception);
   try {
       throw $ex;
   } catch( CacheException $e ) {
       var_dump($e->getMessage());
   }
   ?>

See also `php-psr <https://github.com/jbboehr/php-psr>`_ and `PHP-FIG <https://www.php-fig.org/>`_.

Connex PHP features
-------------------

  + `psr <https://php-dictionary.readthedocs.io/en/latest/dictionary/psr.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpsr                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


