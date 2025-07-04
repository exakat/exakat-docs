.. _extensions-extleveldb:


.. _ext-leveldb:

ext/leveldb
+++++++++++

.. meta::
	:description:
		ext/leveldb: PHP Binding for LevelDB.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/leveldb
	:twitter:description: ext/leveldb: PHP Binding for LevelDB
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/leveldb
	:og:type: article
	:og:description: PHP Binding for LevelDB
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/leveldb.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extleveldb.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extleveldb.html","name":"ext\/leveldb","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"PHP Binding for LevelDB","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/leveldb.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP Binding for LevelDB.

LevelDB is a fast key-value storage library written at Google that provides an ordered mapping from string keys to string values.

.. code-block:: php
   
   <?php
   
   $db = new LevelDB($leveldb_path);
   
   $batch = new LevelDBWriteBatch();
   $batch->set('batch_foo', 'batch_bar');
   $batch->put('batch_foo2', 'batch_bar2');
   $batch->delete('batch_foo');
   
   $db->write($batch);
   
   $batch->clear();
   $batch->delete('batch_foo2');
   $batch->set('batch_foo', 'batch again');
   
   ?>

See also `ext/leveldb on Github <https://github.com/reeze/php-leveldb>`_ and `Leveldb <https://github.com/google/leveldb>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extleveldb                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                                                                                   |
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


