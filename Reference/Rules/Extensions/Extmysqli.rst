.. _extensions-extmysqli:


.. _ext-mysqli:

ext/mysqli
++++++++++

.. meta::
	:description:
		ext/mysqli: Extension mysqli for MySQL.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/mysqli
	:twitter:description: ext/mysqli: Extension mysqli for MySQL
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/mysqli
	:og:type: article
	:og:description: Extension mysqli for MySQL
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/mysqli.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extmysqli.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extmysqli.html","name":"ext\/mysqli","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension mysqli for MySQL","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/mysqli.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension `mysqli <https://www.php.net/mysqli>`_ for MySQL.

The `mysqli <https://www.php.net/mysqli>`_ extension allows you to access the functionality provided by MySQL 4.1 and above.

.. code-block:: php
   
   <?php
   $mysqli = new mysqli('localhost', 'my_user', 'my_password', 'world');
   
   /* check connection */
   if (mysqli_connect_errno()) {
       printf('Connect failed: %s\n', mysqli_connect_error());
       exit();
   }
   
   $city = 'Amersfoort';
   
   /* create a prepared statement */
   if ($stmt = $mysqli->prepare('SELECT District FROM City WHERE Name=?')) {
   
       /* bind parameters for markers */
       $stmt->bind_param('s', $city);
   
       /* execute query */
       $stmt->execute();
   
       /* bind result variables */
       $stmt->bind_result($district);
   
       /* fetch value */
       $stmt->fetch();
   
       printf('%s is in district %s\n', $city, $district);
   
       /* close statement */
       $stmt->close();
   }
   
   /* close connection */
   $mysqli->close();
   ?>

See also `MySQL Improved Extension <https://www.php.net/manual/en/book.mysqli.php>`_, `MySQL <https://www.mysql.com/>`_ and `Mariadb <https://mariadb.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extmysqli                                                                                                                                                                    |
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


