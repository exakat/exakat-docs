.. _vendors-phalcon:

.. _phalcon-usage:

Phalcon Usage
+++++++++++++

  This analysis reports usage of the Phalcon Framework. The report is based on the usage of Phalcon namespace, which may be provided by PHP code inclusion or the PHP extension.

.. code-block:: php
   
   <?php
   
   use Phalcon\Mvc\Application;
   
   // Register autoloaders
   
   // Register services
   
   // Handle the request
   $application = new Application($di);
   
   try {
       $response = $application->handle();
   
       $response->send();
   } catch (\Exception $e) {
       echo 'Exception: ', $e->getMessage();
   }
   
   ?>

See also `Phalcon <https://phalconphp.com/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Phalcon                                                                                                                                                                         |
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


