.. _extensions-exthttp:

.. _ext-pecl\_http:

ext/pecl_http
+++++++++++++

  Extension HTTP.

This HTTP extension aims to provide a convenient and powerful set of functionalities for one of PHP major applications.

It eases handling of HTTP URL, headers and messages, provides means for negotiation of a client's preferred content type, language and charset, as well as a convenient way to send any arbitrary data with caching and resuming capabilities.

It provides powerful request functionality with support for parallel requests.

.. code-block:: php
   
   <?php 
   
   $client = new http\Client;
   $client->setSslOptions(array("verifypeer" => true));
   $client->addSslOptions(array("verifyhost" => 2));
   
   $client->enqueue($req = new http\Client\Request("GET", "https://twitter.com/"));
   $client->send();
   $ti = (array) $client->getTransferInfo($req);
   var_dump($ti);
   
   ?>

See also `ext-http <https://github.com/m6w6/ext-http>`_ and `pecl_http <https://pecl.php.net/package/pecl_http>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exthttp                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


