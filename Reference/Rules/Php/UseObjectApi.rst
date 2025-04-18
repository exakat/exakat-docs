.. _php-useobjectapi:


.. _use-php-object-api:

Use PHP Object API
++++++++++++++++++

.. meta::
	:description:
		Use PHP Object API: OOP API is the modern version of the PHP API.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use PHP Object API
	:twitter:description: Use PHP Object API: OOP API is the modern version of the PHP API
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use PHP Object API
	:og:type: article
	:og:description: OOP API is the modern version of the PHP API
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use PHP Object API.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseObjectApi.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseObjectApi.html","name":"Use PHP Object API","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"OOP API is the modern version of the PHP API","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use PHP Object API.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

OOP API is the modern version of the PHP API.

When PHP offers the alternative between procedural and OOP api for the same features, it is recommended to use the OOP API. 

Often, this least to more compact code, as methods are shorter, and there is no need to bring the resource around. Lots of new extensions are directly written in OOP form too.

OOP / procedural alternatives are available for `mysqli <https://www.php.net/manual/en/book.`mysqli <https://www.php.net/mysqli>`_.php>`_, `tidy <https://www.php.net/manual/en/book.`tidy <https://www.php.net/tidy>`_.php>`_, `cairo <https://www.php.net/manual/en/book.cairo.php>`_, `finfo <https://www.php.net/manual/en/book.fileinfo.php>`_, and some others.

.. code-block:: php
   
   <?php
   /// OOP version
   $mysqli = new mysqli("localhost", "my_user", "my_password", "world");
   
   /* check connection */
   if ($mysqli->connect_errno) {
       printf("Connect failed: %s\n", $mysqli->connect_error);
       exit();
   }
   
   /* Create table doesn't return a resultset */
   if ($mysqli->query("CREATE TEMPORARY TABLE myCity LIKE City") === TRUE) {
       printf("Table myCity successfully created.\n");
   }
   
   /* Select queries return a resultset */
   if ($result = $mysqli->query("SELECT Name FROM City LIMIT 10")) {
       printf("Select returned %d rows.\n", $result->num_rows);
   
       /* free result set */
       $result->close();
   }
   ?>
Connex PHP features
-------------------

  + `Object API <https://php-dictionary.readthedocs.io/en/latest/dictionary/object-api.ini.html>`_


Suggestions
___________

* Use the object API




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseObjectApi                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `use-object-api <https://github.com/dseguy/clearPHP/tree/master/rules/use-object-api.md>`__                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-php-useobjectapi`, :ref:`case-prestashop-php-useobjectapi`                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


