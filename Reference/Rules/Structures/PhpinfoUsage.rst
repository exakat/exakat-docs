.. _structures-phpinfousage:

.. _phpinfo:

Phpinfo
+++++++

.. meta::
	:description:
		Phpinfo: phpinfo() is a great function to learn about the current configuration of the server.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Phpinfo
	:twitter:description: Phpinfo: phpinfo() is a great function to learn about the current configuration of the server
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Phpinfo
	:og:type: article
	:og:description: phpinfo() is a great function to learn about the current configuration of the server
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Phpinfo.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PhpinfoUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PhpinfoUsage.html","name":"Phpinfo","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"phpinfo() is a great function to learn about the current configuration of the server","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Phpinfo.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`phpinfo() <https://www.php.net/phpinfo>`_ is a great function to learn about the current configuration of the server.
If left in the production code, it may lead to a critical leak, as any attacker gaining access to this data will know a lot about the server configuration.

It is advised to never leave that kind of instruction in a production code. 

`phpinfo() <https://www.php.net/phpinfo>`_ may be necessary to access some specific configuration of the server : for example, ``Apache`` module list are only available via `phpinfo() <https://www.php.net/phpinfo>`_, and apache_get(), when they are loaded.

.. code-block:: php
   
   <?php
   
   if (DEBUG) {
       phpinfo();
   }
   
   ?>
Connex PHP features
-------------------

  + `phpinfo <https://php-dictionary.readthedocs.io/en/latest/dictionary/phpinfo.ini.html>`_


Suggestions
___________

* Remove all usage of phpinfo()
* Add one or more constant to fine-tune the phpinfo(), and limit the amount of displayed information
* Replace phpinfo() with a more adapted method : get_loaded_extensions() to access the list of loaded extensions




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PhpinfoUsage                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-structures-phpinfousage`                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


