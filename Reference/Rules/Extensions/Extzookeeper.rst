.. _extensions-extzookeeper:

.. _ext-zookeeper:

ext/zookeeper
+++++++++++++

.. meta::
	:description:
		ext/zookeeper: Extension for Apache Zookeeper.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/zookeeper
	:twitter:description: ext/zookeeper: Extension for Apache Zookeeper
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/zookeeper
	:og:type: article
	:og:description: Extension for Apache Zookeeper
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/zookeeper.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extzookeeper.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extzookeeper.html","name":"ext\/zookeeper","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension for Apache Zookeeper","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/zookeeper.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension for Apache Zookeeper. 

ZooKeeper is an Apache project that enables centralized service for maintaining configuration information, naming, providing distributed synchronization, and providing group services.

.. code-block:: php
   
   <?php
   $zookeeper = new Zookeeper('locahost:2181');
   $path = '/path/to/node';
   $value = 'nodevalue';
   $zookeeper->set($path, $value);
   
   $r = $zookeeper->get($path);
   if ($r)
     echo $r;
   else
     echo 'ERR';
   ?>

See also `ext/zookeeper <https://www.php.net/zookeeper>`_, `Install Zookeeper PHP Extension <https://blog.programster.org/install-zookeeper-php-extension>`_ and `Zookeeper <https://zookeeper.apache.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extzookeeper                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


