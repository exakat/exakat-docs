.. _security-cantdisableclass:

.. _can't-disable-class:

Can't Disable Class
+++++++++++++++++++

.. meta::
	:description:
		Can't Disable Class: This is the list of potentially dangerous PHP class being used in the code, such as \Phar.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Disable Class
	:twitter:description: Can't Disable Class: This is the list of potentially dangerous PHP class being used in the code, such as \Phar
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Disable Class
	:og:type: article
	:og:description: This is the list of potentially dangerous PHP class being used in the code, such as \Phar
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Can't Disable Class.html
	:og:locale: en
This is the list of potentially dangerous PHP class being used in the code, such as \`Phar <https://www.php.net/phar>`_. 
This analysis is the base for suggesting values for the ``disable_classes`` directive.

.. code-block:: php
   
   <?php
   
   // This script uses ftp_connect(), therefore, this function shouldn't be disabled. 
   $phar = new Phar();
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/X%28%29+has+been+disabled+for+security+reasons.html>`_



Connex PHP features
-------------------

  + `disable-classes <https://php-dictionary.readthedocs.io/en/latest/dictionary/disable-classes.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/CantDisableClass                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`can't-disable-function`                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


