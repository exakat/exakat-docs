.. _extensions-extpdo:

.. _ext-pdo:

ext/pdo
+++++++

.. meta\:\:
	:description:
		ext/pdo: Generic extension PDO.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/pdo
	:twitter:description: ext/pdo: Generic extension PDO
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/pdo
	:og:type: article
	:og:description: Generic extension PDO
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extpdo.html
	:og:locale: en
  Generic extension `PDO <https://www.php.net/pdo>`_.

The PHP Data Objects (`PDO) <https://www.php.net/pdo>`_ extension defines a lightweight, consistent interface for accessing databases in PHP.

.. code-block:: php
   
   <?php
   /* Execute a prepared statement by passing an array of values */
   $sql = 'SELECT name, colour, calories
       FROM fruit
       WHERE calories < :calories AND colour = :colour';
   $sth = $dbh->prepare($sql, array(PDO::ATTR_CURSOR => PDO::CURSOR_FWDONLY));
   $sth->execute(array(':calories' => 150, ':colour' => 'red'));
   $red = $sth->fetchAll();
   $sth->execute(array(':calories' => 175, ':colour' => 'yellow'));
   $yellow = $sth->fetchAll();
   ?>

See also `PHP Data Object <https://www.php.net/manual/en/book.pdo.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpdo                                                                                                                                                                       |
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


