.. _extensions-extmongo:

.. _ext-mongo:

ext/mongo
+++++++++

  Extension `MongoDB <https://www.php.net/MongoDB>`_ driver (legacy).
Note : this is not the `MongoDB driver <https://www.php.net/mongo>`_. This is the legacy extension.

.. code-block:: php
   
   <?php
   
   // connect
   $m = new MongoClient();
   
   // select a database
   $db = $m->comedy;
   
   // select a collection (analogous to a relational database\'s table)
   $collection = $db->cartoons;
   
   // add a record
   $document = array( 'title' => 'Calvin and Hobbes', 'author' => 'Bill Watterson' );
   $collection->insert($document);
   
   // add another record, with a different 'shape'
   $document = array( 'title' => 'XKCD', 'online' => true );
   $collection->insert($document);
   
   // find everything in the collection
   $cursor = $collection->find();
   
   // iterate through the results
   foreach ($cursor as $document) {
       echo $document['title'] . PHP_EOL;
   }
   
   ?>

See also `ext/mongo manual <https://www.php.net/manual/en/book.mongo.php>`_ and `MongdDb <https://www.mongodb.com/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmongo                                                                                                                                                                     |
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


