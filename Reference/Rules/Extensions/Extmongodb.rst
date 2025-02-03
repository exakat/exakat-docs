.. _extensions-extmongodb:

.. _ext-mongodb:

ext/mongodb
+++++++++++

.. meta::
	:description:
		ext/mongodb: Extension MongoDb.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/mongodb
	:twitter:description: ext/mongodb: Extension MongoDb
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/mongodb
	:og:type: article
	:og:description: Extension MongoDb
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/mongodb.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extmongodb.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extmongodb.html","name":"ext\/mongodb","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension MongoDb","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/mongodb.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension MongoDb.

Do not mistake with extension `Mongo <https://www.php.net/Mongo>`_, the previous version.

Mongodb driver supports both PHP and HHVM and is developed atop the `libmongoc <https://github.com/mongodb/mongo-c-driver>`_ and `libbson <https://github.com/mongodb/libbson>`_ libraries.

.. code-block:: php
   
   <?php
   require 'vendor/autoload.php'; // include Composer's autoloader
   
   $client = new MongoDB\Client("mongodb://localhost:27017");
   $collection = $client->demo->beers;
   
   $result = $collection->insertOne( [ 'name' => 'Hinterland', 'brewery' => 'BrewDog' ] );
   
   echo "Inserted with Object ID '{$result->getInsertedId()}'";
   ?>

See also `MongoDB driver <https://www.php.net/manual/en/set.mongodb.php>`_ and `MongdDb <https://www.mongodb.com/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmongodb                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.5                                                                                                                                                                                   |
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


